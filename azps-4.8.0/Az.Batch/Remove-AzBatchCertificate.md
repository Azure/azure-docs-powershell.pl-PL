---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3DFFD0F2-6CD8-4FBE-B15C-8505CBF8F44E
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchCertificate.md
ms.openlocfilehash: 2f751a6efcf4b798c69bb0dfd9ecd38c33a65d01
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064537"
---
# <span data-ttu-id="1845c-101">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="1845c-101">Remove-AzBatchCertificate</span></span>

## <span data-ttu-id="1845c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1845c-102">SYNOPSIS</span></span>
<span data-ttu-id="1845c-103">Usuwa certyfikat z konta.</span><span class="sxs-lookup"><span data-stu-id="1845c-103">Deletes a certificate from an account.</span></span>

## <span data-ttu-id="1845c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1845c-104">SYNTAX</span></span>

```
Remove-AzBatchCertificate [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1845c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1845c-105">DESCRIPTION</span></span>
<span data-ttu-id="1845c-106">Polecenie cmdlet **Remove-AzBatchCertificate** usuwa certyfikat z określonego konta usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="1845c-106">The **Remove-AzBatchCertificate** cmdlet removes a certificate from the specified Azure Batch account.</span></span>

## <span data-ttu-id="1845c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1845c-107">EXAMPLES</span></span>

### <span data-ttu-id="1845c-108">Przykład 1. Usuń certyfikat</span><span class="sxs-lookup"><span data-stu-id="1845c-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzBatchCertificate -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="1845c-109">To polecenie usuwa certyfikat z określonym odciskiem palca.</span><span class="sxs-lookup"><span data-stu-id="1845c-109">This command removes the certificate that has the specified thumbprint.</span></span>

### <span data-ttu-id="1845c-110">Przykład 2: Usuwanie wszystkich aktywnych certyfikatów</span><span class="sxs-lookup"><span data-stu-id="1845c-110">Example 2:Remove all active certificates</span></span>
```
PS C:\>Get-AzBatchCertificate -Filter "state eq 'active'" -BatchContext $Context | Remove-AzBatchCertificate -Force -BatchContext $Context
```

<span data-ttu-id="1845c-111">To polecenie pobiera wszystkie aktywne certyfikaty za pomocą polecenia cmdlet Get-AzBatchCertificate.</span><span class="sxs-lookup"><span data-stu-id="1845c-111">This command gets all certificates that are active by using the Get-AzBatchCertificate cmdlet.</span></span>
<span data-ttu-id="1845c-112">Polecenie przekazuje aktywne certyfikaty do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="1845c-112">The command passes the active certificates to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1845c-113">Polecenie cmdlet powoduje usunięcie każdego certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="1845c-113">That cmdlet removes each certificate.</span></span>
<span data-ttu-id="1845c-114">Polecenie określa parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="1845c-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="1845c-115">Dlatego polecenie nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1845c-115">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="1845c-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1845c-116">PARAMETERS</span></span>

### <span data-ttu-id="1845c-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="1845c-117">-BatchContext</span></span>
<span data-ttu-id="1845c-118">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="1845c-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="1845c-119">Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="1845c-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="1845c-120">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKey, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="1845c-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="1845c-121">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="1845c-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="1845c-122">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="1845c-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="1845c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1845c-123">-DefaultProfile</span></span>
<span data-ttu-id="1845c-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1845c-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1845c-125">-Odcisk palca</span><span class="sxs-lookup"><span data-stu-id="1845c-125">-Thumbprint</span></span>
<span data-ttu-id="1845c-126">Określa odcisk palca certyfikatu usuniętego przez ten aplet polecenia.</span><span class="sxs-lookup"><span data-stu-id="1845c-126">Specifies the thumbprint of the certificate that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="1845c-127">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="1845c-127">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="1845c-128">Określa algorytm używany do uzyskania parametru *odcisku palca* .</span><span class="sxs-lookup"><span data-stu-id="1845c-128">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="1845c-129">Obecnie jedyną prawidłową wartością jest SHA1.</span><span class="sxs-lookup"><span data-stu-id="1845c-129">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="1845c-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1845c-130">-Confirm</span></span>
<span data-ttu-id="1845c-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1845c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1845c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1845c-132">-WhatIf</span></span>
<span data-ttu-id="1845c-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1845c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1845c-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1845c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1845c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1845c-135">CommonParameters</span></span>
<span data-ttu-id="1845c-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1845c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1845c-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1845c-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1845c-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1845c-138">INPUTS</span></span>

### <span data-ttu-id="1845c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="1845c-139">System.String</span></span>

### <span data-ttu-id="1845c-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="1845c-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="1845c-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1845c-141">OUTPUTS</span></span>

### <span data-ttu-id="1845c-142">System. void</span><span class="sxs-lookup"><span data-stu-id="1845c-142">System.Void</span></span>

## <span data-ttu-id="1845c-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1845c-143">NOTES</span></span>

## <span data-ttu-id="1845c-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1845c-144">RELATED LINKS</span></span>

[<span data-ttu-id="1845c-145">Get-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="1845c-145">Get-AzBatchCertificate</span></span>](./Get-AzBatchCertificate.md)

[<span data-ttu-id="1845c-146">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="1845c-146">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="1845c-147">Nowe — AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="1845c-147">New-AzBatchCertificate</span></span>](./New-AzBatchCertificate.md)

[<span data-ttu-id="1845c-148">Zatrzymaj — AzBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="1845c-148">Stop-AzBatchCertificateDeletion</span></span>](./Stop-AzBatchCertificateDeletion.md)

[<span data-ttu-id="1845c-149">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="1845c-149">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
