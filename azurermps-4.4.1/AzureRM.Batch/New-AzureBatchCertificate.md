---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B423C1A1-1988-4721-81E7-3B7EC163B03A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchCertificate.md
ms.openlocfilehash: d567c176580cba0659d6c88c919ffa34cad393ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719536"
---
# New-AzureBatchCertificate

## STRESZCZENIe
Dodaje certyfikat do określonego konta wsadowego.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### Plik (domyślnie)
```
New-AzureBatchCertificate [-FilePath] <String> [-Password <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### RawData
```
New-AzureBatchCertificate [-RawData] <Byte[]> [-Password <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzureBatchCertificate** umożliwia dodanie certyfikatu do określonego konta usługi Azure Batch.

## Przykłady

### Przykład 1: Dodawanie certyfikatu z pliku
```
PS C:\>New-AzureBatchCertificate -FilePath "E:\Certificates\MyCert.cer" -BatchContext $Context
```

To polecenie dodaje certyfikat do określonego konta wsadowego przy użyciu pliku E:\Certificates\MyCert.cer.

### Przykład 2: Dodawanie certyfikatu z danych nieprzetworzonych
```
PS C:\>$RawData = [System.IO.File]::ReadAllBytes("E:\Certificates\MyCert.pfx")
PS C:\> New-AzureBatchCertificate -RawData $RawData -Password "Password1234" -BatchContext $Context
```

Pierwsze polecenie odczytuje dane z pliku o nazwie Moje CERT. pfx do zmiennej $RawData.

Drugie polecenie dodaje certyfikat do określonego konta wsadowego przy użyciu danych pierwotnych przechowywanych w $RawData.

## PARAMETRÓW

### -BatchContext
Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.
Aby uzyskać obiekt **BatchAccountContext** , który zawiera klucze dostępu dla subskrypcji, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys.

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -FilePath
Określa ścieżkę pliku certyfikatu.
Plik certyfikatu musi znajdować się w formacie cer lub PFX.

```yaml
Type: System.String
Parameter Sets: File
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Password (hasło)
Określa hasło dostępu do prywatnego klucza certyfikatu.
Jeśli określisz certyfikat w formacie PFX, musisz określić ten parametr.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RawData
Określa dane certyfikatu surowego w formacie cer lub PFX.

```yaml
Type: System.Byte[]
Parameter Sets: RawData
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### BatchAccountContext
Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu

### Byte []
Parametr "RawData" akceptuje wartość typu "Byte []" z procesu

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureBatchCertificate](./Get-AzureBatchCertificate.md)

[Get-AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[Remove-AzureBatchCertificate](./Remove-AzureBatchCertificate.md)

[Polecenia cmdlet usługi Azure Batch](./AzureRM.Batch.md)


