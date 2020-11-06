---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 3DFFD0F2-6CD8-4FBE-B15C-8505CBF8F44E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchCertificate.md
ms.openlocfilehash: 7e8159a7a17276d749adb89ea4e1b82118f9b2bd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547580"
---
# <span data-ttu-id="b292a-101">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="b292a-101">Remove-AzureBatchCertificate</span></span>

## <span data-ttu-id="b292a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b292a-102">SYNOPSIS</span></span>
<span data-ttu-id="b292a-103">Usuwa certyfikat z konta.</span><span class="sxs-lookup"><span data-stu-id="b292a-103">Deletes a certificate from an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b292a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b292a-104">SYNTAX</span></span>

```
Remove-AzureBatchCertificate [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b292a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b292a-105">DESCRIPTION</span></span>
<span data-ttu-id="b292a-106">Polecenie cmdlet **Remove-AzureBatchCertificate** usuwa certyfikat z określonego konta usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="b292a-106">The **Remove-AzureBatchCertificate** cmdlet removes a certificate from the specified Azure Batch account.</span></span>

## <span data-ttu-id="b292a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b292a-107">EXAMPLES</span></span>

### <span data-ttu-id="b292a-108">Przykład 1. Usuń certyfikat</span><span class="sxs-lookup"><span data-stu-id="b292a-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureBatchCertificate -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="b292a-109">To polecenie usuwa certyfikat z określonym odciskiem palca.</span><span class="sxs-lookup"><span data-stu-id="b292a-109">This command removes the certificate that has the specified thumbprint.</span></span>

### <span data-ttu-id="b292a-110">Przykład 2: Usuwanie wszystkich aktywnych certyfikatów</span><span class="sxs-lookup"><span data-stu-id="b292a-110">Example 2:Remove all active certificates</span></span>
```
PS C:\>Get-AzureBatchCertificate -Filter "state eq 'active'" -BatchContext $Context | Remove-AzureBatchCertificate -Force -BatchContext $Context
```

<span data-ttu-id="b292a-111">To polecenie pobiera wszystkie aktywne certyfikaty za pomocą polecenia cmdlet Get-AzureBatchCertificate.</span><span class="sxs-lookup"><span data-stu-id="b292a-111">This command gets all certificates that are active by using the Get-AzureBatchCertificate cmdlet.</span></span>
<span data-ttu-id="b292a-112">Polecenie przekazuje aktywne certyfikaty do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="b292a-112">The command passes the active certificates to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b292a-113">Polecenie cmdlet powoduje usunięcie każdego certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="b292a-113">That cmdlet removes each certificate.</span></span>
<span data-ttu-id="b292a-114">Polecenie określa parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="b292a-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="b292a-115">Dlatego polecenie nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b292a-115">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="b292a-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b292a-116">PARAMETERS</span></span>

### <span data-ttu-id="b292a-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b292a-117">-BatchContext</span></span>
<span data-ttu-id="b292a-118">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="b292a-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b292a-119">Jeśli używasz polecenia cmdlet Get-AzureRmBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="b292a-119">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="b292a-120">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="b292a-120">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="b292a-121">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="b292a-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="b292a-122">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="b292a-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="b292a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b292a-123">-DefaultProfile</span></span>
<span data-ttu-id="b292a-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b292a-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b292a-125">-Odcisk palca</span><span class="sxs-lookup"><span data-stu-id="b292a-125">-Thumbprint</span></span>
<span data-ttu-id="b292a-126">Określa odcisk palca certyfikatu usuniętego przez ten aplet polecenia.</span><span class="sxs-lookup"><span data-stu-id="b292a-126">Specifies the thumbprint of the certificate that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="b292a-127">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="b292a-127">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="b292a-128">Określa algorytm używany do uzyskania parametru *odcisku palca* .</span><span class="sxs-lookup"><span data-stu-id="b292a-128">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="b292a-129">Obecnie jedyną prawidłową wartością jest SHA1.</span><span class="sxs-lookup"><span data-stu-id="b292a-129">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="b292a-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b292a-130">-Confirm</span></span>
<span data-ttu-id="b292a-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b292a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b292a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b292a-132">-WhatIf</span></span>
<span data-ttu-id="b292a-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b292a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b292a-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b292a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b292a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b292a-135">CommonParameters</span></span>
<span data-ttu-id="b292a-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b292a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b292a-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b292a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b292a-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b292a-138">INPUTS</span></span>

### <span data-ttu-id="b292a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b292a-139">System.String</span></span>

### <span data-ttu-id="b292a-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b292a-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="b292a-141">Parametry: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b292a-141">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="b292a-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b292a-142">OUTPUTS</span></span>

### <span data-ttu-id="b292a-143">System. void</span><span class="sxs-lookup"><span data-stu-id="b292a-143">System.Void</span></span>

## <span data-ttu-id="b292a-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b292a-144">NOTES</span></span>

## <span data-ttu-id="b292a-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b292a-145">RELATED LINKS</span></span>

[<span data-ttu-id="b292a-146">Get-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="b292a-146">Get-AzureBatchCertificate</span></span>](./Get-AzureBatchCertificate.md)

[<span data-ttu-id="b292a-147">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="b292a-147">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="b292a-148">Nowe — AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="b292a-148">New-AzureBatchCertificate</span></span>](./New-AzureBatchCertificate.md)

[<span data-ttu-id="b292a-149">Zatrzymaj — AzureBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="b292a-149">Stop-AzureBatchCertificateDeletion</span></span>](./Stop-AzureBatchCertificateDeletion.md)

[<span data-ttu-id="b292a-150">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="b292a-150">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


