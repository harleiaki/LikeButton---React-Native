https://user-images.githubusercontent.com/96266332/224879360-8a9ef6f3-9429-45b5-a04b-8098ff8c49fc.mp4

import React, {Component} from 'react';

import {StyleSheet, Text, TouchableOpacity, View} from 'react-native';

import { Button } from 'react-native-paper';

import { AntDesign } from '@expo/vector-icons';  //icone relogio,coracao

class App extends Component {

  state = {
    count: 0,
  };

  onPress = () => {
    this.setState({
      count: this.state.count + 1,

    });
  };

  render() {
    return (
      <View style={styles.container}>
        <TouchableOpacity onPress={this.onPress}>
          <View style={styles.button}>
                 <AntDesign name="heart" size={24} color="red" />
          </View>
        </TouchableOpacity>
        <View style={[styles.countContainer]}>
          <Text style={[styles.countText]}>
            {this.state.count ? this.state.count : null}
          </Text>
        </View>
      </View>
    );
  }
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    justifyContent: 'center',

  },
  button: {
    alignItems: 'center',
    

  },
  countContainer: {
    alignItems: 'center',

  },


});

export default App;
