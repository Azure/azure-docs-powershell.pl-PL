---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 3DFFD0F2-6CD8-4FBE-B15C-8505CBF8F44E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchCertificate.md
ms.openlocfilehash: c63caed99a10851d6172e0db5dcc33e3404be215
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528270"
---
# <span data-ttu-id="49dee-101">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="49dee-101">Remove-AzureBatchCertificate</span></span>

## <span data-ttu-id="49dee-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="49dee-102">SYNOPSIS</span></span>
<span data-ttu-id="49dee-103">Usuwa certyfikat z konta.</span><span class="sxs-lookup"><span data-stu-id="49dee-103">Deletes a certificate from an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49dee-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="49dee-104">SYNTAX</span></span>

```
Remove-AzureBatchCertificate [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="49dee-105">Opis</span><span class="sxs-lookup"><span data-stu-id="49dee-105">DESCRIPTION</span></span>
<span data-ttu-id="49dee-106">Polecenie cmdlet **Remove-AzureBatchCertificate** usuwa certyfikat z określonego konta usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="49dee-106">The **Remove-AzureBatchCertificate** cmdlet removes a certificate from the specified Azure Batch account.</span></span>

## <span data-ttu-id="49dee-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="49dee-107">EXAMPLES</span></span>

### <span data-ttu-id="49dee-108">Przykład 1. Usuń certyfikat</span><span class="sxs-lookup"><span data-stu-id="49dee-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureBatchCertificate -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="49dee-109">To polecenie usuwa certyfikat z określonym odciskiem palca.</span><span class="sxs-lookup"><span data-stu-id="49dee-109">This command removes the certificate that has the specified thumbprint.</span></span>

### <span data-ttu-id="49dee-110">Przykład 2: Usuwanie wszystkich aktywnych certyfikatów</span><span class="sxs-lookup"><span data-stu-id="49dee-110">Example 2:Remove all active certificates</span></span>
```
PS C:\>Get-AzureBatchCertificate -Filter "state eq 'active'" -BatchContext $Context | Remove-AzureBatchCertificate -Force -BatchContext $Context
```

<span data-ttu-id="49dee-111">To polecenie pobiera wszystkie aktywne certyfikaty za pomocą polecenia cmdlet Get-AzureBatchCertificate.</span><span class="sxs-lookup"><span data-stu-id="49dee-111">This command gets all certificates that are active by using the Get-AzureBatchCertificate cmdlet.</span></span>
<span data-ttu-id="49dee-112">Polecenie przekazuje aktywne certyfikaty do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="49dee-112">The command passes the active certificates to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="49dee-113">Polecenie cmdlet powoduje usunięcie każdego certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="49dee-113">That cmdlet removes each certificate.</span></span>
<span data-ttu-id="49dee-114">Polecenie określa parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="49dee-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="49dee-115">Dlatego polecenie nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="49dee-115">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="49dee-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="49dee-116">PARAMETERS</span></span>

### <span data-ttu-id="49dee-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="49dee-117">-BatchContext</span></span>
<span data-ttu-id="49dee-118">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="49dee-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="49dee-119">Aby uzyskać obiekt **BatchAccountContext** , który zawiera klucze dostępu dla subskrypcji, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="49dee-119">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="49dee-120">-Odcisk palca</span><span class="sxs-lookup"><span data-stu-id="49dee-120">-Thumbprint</span></span>
<span data-ttu-id="49dee-121">Określa odcisk palca certyfikatu usuniętego przez ten aplet polecenia.</span><span class="sxs-lookup"><span data-stu-id="49dee-121">Specifies the thumbprint of the certificate that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49dee-122">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="49dee-122">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="49dee-123">Określa algorytm używany do uzyskania parametru *odcisku palca* .</span><span class="sxs-lookup"><span data-stu-id="49dee-123">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="49dee-124">Obecnie jedyną prawidłową wartością jest SHA1.</span><span class="sxs-lookup"><span data-stu-id="49dee-124">Currently, the only valid value is sha1.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49dee-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="49dee-125">-Confirm</span></span>
<span data-ttu-id="49dee-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49dee-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49dee-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49dee-127">-WhatIf</span></span>
<span data-ttu-id="49dee-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49dee-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49dee-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="49dee-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49dee-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49dee-130">-DefaultProfile</span></span>
<span data-ttu-id="49dee-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="49dee-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49dee-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49dee-132">CommonParameters</span></span>
<span data-ttu-id="49dee-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49dee-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49dee-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49dee-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49dee-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49dee-135">INPUTS</span></span>

### <span data-ttu-id="49dee-136">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="49dee-136">BatchAccountContext</span></span>
<span data-ttu-id="49dee-137">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="49dee-137">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="49dee-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="49dee-138">OUTPUTS</span></span>

## <span data-ttu-id="49dee-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="49dee-139">NOTES</span></span>

## <span data-ttu-id="49dee-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="49dee-140">RELATED LINKS</span></span>

[<span data-ttu-id="49dee-141">Get-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="49dee-141">Get-AzureBatchCertificate</span></span>](./Get-AzureBatchCertificate.md)

[<span data-ttu-id="49dee-142">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="49dee-142">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="49dee-143">Nowe — AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="49dee-143">New-AzureBatchCertificate</span></span>](./New-AzureBatchCertificate.md)

[<span data-ttu-id="49dee-144">Zatrzymaj — AzureBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="49dee-144">Stop-AzureBatchCertificateDeletion</span></span>](./Stop-AzureBatchCertificateDeletion.md)

[<span data-ttu-id="49dee-145">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="49dee-145">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


