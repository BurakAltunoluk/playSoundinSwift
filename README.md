# playSoundinSwift
How to play a sound using Swift? 

```swift 
import UIKit
import AVFoundation

class ViewController: UIViewController {
    
    var player: AVAudioPlayer!

    override func viewDidLoad() {
        super.viewDidLoad()
    }

    @IBAction func keyPressed(_ sender: UIButton) {
        playSound()
    }
    
    func playSound() {
        let url = Bundle.main.url(forResource: "sound1", withExtension: "mp3")
        player = try! AVAudioPlayer(contentsOf: url!)
        player.play()
                
    }
}
//---------WITH URL-------------

import UIKit
import AVFoundation
import AVKit


HTTP 
info.playlist -> App Trasport Security setting -> Allow Arbitrary Loads -> YES



    var player: AVPlayer?
    func playSound(url: String) {
                    guard let url = URL.init(string: url)
                        else {
                            return
                    }
                    let playerItem = AVPlayerItem.init(url: url)
                    player = AVPlayer.init(playerItem: playerItem)
                player?.play()
    }
