---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5008F83F-AF3E-47CF-99A3-55129E654128
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSecret.md
ms.openlocfilehash: b6d5d7b68726d1e5121491a6b4c5b371a9ec7cec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869164"
---
# Add-AzVMSecret

## STRESZCZENIe
Dodaje klucz tajny do maszyny wirtualnej.

## POLECENIA

```
Add-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String>] [[-CertificateStore] <String>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Add-AzVMSecret** umożliwia dodanie klucza tajnego do maszyny wirtualnej.
Ta wartość umożliwia dodanie certyfikatu do maszyny wirtualnej.
Klucz tajny musi być przechowywany w magazynie kluczy.
Aby uzyskać więcej informacji na temat magazynu kluczy, zobacz [co to jest magazyn kluczy Azure?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).
Aby uzyskać więcej informacji na temat poleceń cmdlet, zobacz [polecenia cmdlet magazynu kluczy platformy Azure](https://msdn.microsoft.com/library/azure/dn868052.aspx) w bibliotece sieci Microsoft Developer Network lub polecenia cmdlet [Set-AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) .

## Przykłady

### Przykład 1: Dodawanie klucza tajnego do maszyny wirtualnej
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $SourceVaultId = "/subscriptions/46f8cea4-2de6-4179-8ab1-365da4211af4/resourceGroups/vault/providers/Microsoft.KeyVault/vaults/keyvault"
PS C:\> $CertificateStore01 = "My"
PS C:\> $CertificateUrl01 = "https://contosovault.vault.azure.net/secrets/514ceb769c984379a7e0230bdd703272"
PS C:\> $VirtualMachine = Add-AzVMSecret -VM $VirtualMachine -SourceVaultId $SourceVaultId -CertificateStore $CertificateStore01 -CertificateUrl $CertificateUrl01
```

Pierwsze polecenie tworzy obiekt maszyny wirtualnej, a następnie zapisuje go w zmiennej $VirtualMachine.
Polecenie przypisuje nazwę i rozmiar maszynie wirtualnej.
Drugie polecenie tworzy obiekt Credential, korzystając z polecenia cmdlet Get-Credential, a następnie zapisuje wynik w zmiennej $Credential.
Polecenie monituje o podanie nazwy użytkownika i hasła.
Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Credential` .
W trzecim poleceniu jest używana funkcja cmdlet **Set-AzVMOperatingSystem** w celu skonfigurowania maszyny wirtualnej przechowywanej w $VirtualMachine.
Czwarte polecenie przypisuje identyfikator magazynu źródłowego do zmiennej $SourceVaultId w celu późniejszego użycia.
W poleceniu przyjęto założenie, że zmienna $SubscriptionId ma odpowiednią wartość.
Piąte polecenie przypisuje wartość zmiennej $CertificateStore 01 do późniejszego użycia.
Po szóstym poleceniu jest przypisywany adres URL magazynu certyfikatów.
Polecenie siódme powoduje dodanie klucza tajnego do maszyny wirtualnej przechowywanej w $VirtualMachine.
Parametr SourceVaultId określa Magazyn kluczy.
Polecenie określa nazwę magazynu certyfikatów oraz adres URL certyfikatu.
Możesz wielokrotnie uruchamiać **dodatek Add-AzVMSecret** , aby dodać klucze tajne dla innych certyfikatów.

## PARAMETRÓW

### -CertificateStore
Określa nazwę magazynu certyfikatów na maszynie wirtualnej z uruchomionym systemem operacyjnym Windows.
To polecenie cmdlet umożliwia dodanie certyfikatu do magazynu, który określa ten parametr.
Ten parametr można określić tylko dla maszyn wirtualnych, na których jest uruchomiony system operacyjny Windows.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CertificateUrl
Określa adres URL wskazujący klucz tajny magazynu kluczy zawierający certyfikat.
Certyfikat jest kodowaniem Base64 następującego obiektu notacji języka JavaScript (JSON), który jest zakodowany w formacie UTF-8: {"dane": " \< unbase Base64-File", "DataType": " \> \< plik-format \> ", "hasło": " \< PFX-File-Password \> "} obecnie typ danych akceptuje tylko pliki PFX.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceVaultId
Określa identyfikator zasobu magazynu kluczy zawierającego certyfikaty, które można dodać do maszyny wirtualnej.
Ta wartość działa także jako klucz do dodawania wielu certyfikatów.
Oznacza to, że przy dodawaniu wielu certyfikatów z tego samego magazynu kluczy można użyć tej samej wartości dla *SourceVaultId* .

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Określa obiekt maszyny wirtualnej, który jest modyfikowany przez to polecenie cmdlet.
Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet [Get-AzVM](./Get-AzVM.md) .
Za pomocą polecenia cmdlet [New-AzVMConfig](./New-AzVMConfig.md) można utworzyć obiekt maszyny wirtualnej.

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine

### System. String

## WYSYŁA

### Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine

## INFORMACYJN

## LINKI POKREWNE

[Get-AzVM](./Get-AzVM.md)

[Nowe — AzVMConfig](./New-AzVMConfig.md)

[Set-AzVMOperatingSystem](./Set-AzVMOperatingSystem.md)
