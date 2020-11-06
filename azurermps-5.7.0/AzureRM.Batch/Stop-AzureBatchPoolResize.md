---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 3E736E85-0488-4D10-BEA1-4F9B8DA54C4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchPoolResize.md
ms.openlocfilehash: 153e566df3e2ab6f758d139719af1e812e0476ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527061"
---
# Stop-AzureBatchPoolResize

## STRESZCZENIe
Zatrzymuje operację zmiany rozmiaru puli.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Stop-AzureBatchPoolResize [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **stop-AzureBatchPoolResize** zatrzymuje operację zmiany rozmiaru wsadu Azure Part na puli.

## Przykłady

### Przykład 1. Zatrzymaj zmianę rozmiaru puli
```
PS C:\>Stop-AzureBatchPoolResize -Id "ContosoPool06" -BatchContext $Context
```

To polecenie zatrzymuje operację zmiany rozmiaru puli o IDENTYFIKATORze ContosoPool06.
Użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby przypisać kontekst do zmiennej $Context.

### Przykład 2: zatrzymywanie zmiany rozmiaru puli za pomocą potoku
```
PS C:\>Get-AzureBatchPool -Id "ContosoPool06" -BatchContext $Context | Stop-AzureBatchPoolResize -BatchContext $Context
```

To polecenie zatrzymuje zmianę rozmiaru puli za pomocą operatora potoku.
Polecenie pobiera pulę o IDENTYFIKATORze ContosoPool06 przy użyciu polecenia cmdlet Get-AzureBatchPool.
Polecenie przekazuje ten obiekt puli do bieżącego polecenia cmdlet.
Polecenie zatrzyma operację zmiany rozmiaru w tej puli.

## PARAMETRÓW

### -BatchContext
Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.
Jeśli używasz polecenia cmdlet Get-AzureRmBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego. Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu. W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu. Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Określa identyfikator puli, dla którego to polecenie cmdlet zatrzyma operację zmiany rozmiaru.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### BatchAccountContext
Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu

### Ciąg
Parametr "ID" akceptuje wartość typu "String" z procesu

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[Get-AzureBatchPool](./Get-AzureBatchPool.md)

[Start — AzureBatchPoolResize](./Start-AzureBatchPoolResize.md)

[Polecenia cmdlet usługi Azure Batch](./AzureRM.Batch.md)


