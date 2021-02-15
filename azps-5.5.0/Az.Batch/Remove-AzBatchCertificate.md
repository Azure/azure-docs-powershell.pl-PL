---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3DFFD0F2-6CD8-4FBE-B15C-8505CBF8F44E
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchCertificate.md
ms.openlocfilehash: 2f751a6efcf4b798c69bb0dfd9ecd38c33a65d01
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195227"
---
# <span data-ttu-id="4b6a2-101">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="4b6a2-101">Remove-AzBatchCertificate</span></span>

## <span data-ttu-id="4b6a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b6a2-102">SYNOPSIS</span></span>
<span data-ttu-id="4b6a2-103">Usuwa certyfikat z konta.</span><span class="sxs-lookup"><span data-stu-id="4b6a2-103">Deletes a certificate from an account.</span></span>

## <span data-ttu-id="4b6a2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4b6a2-104">SYNTAX</span></span>

```
Remove-AzBatchCertificate [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4b6a2-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="4b6a2-105">DESCRIPTION</span></span>
<span data-ttu-id="4b6a2-106">Polecenie **cmdlet Remove-AzBatchCertificate** usuwa certyfikat z określonego konta usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="4b6a2-106">The **Remove-AzBatchCertificate** cmdlet removes a certificate from the specified Azure Batch account.</span></span>

## <span data-ttu-id="4b6a2-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4b6a2-107">EXAMPLES</span></span>

### <span data-ttu-id="4b6a2-108">Przykład 1. Usuwanie certyfikatu</span><span class="sxs-lookup"><span data-stu-id="4b6a2-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzBatchCertificate -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="4b6a2-109">To polecenie usuwa certyfikat z określonym znakiem usbprint.</span><span class="sxs-lookup"><span data-stu-id="4b6a2-109">This command removes the certificate that has the specified thumbprint.</span></span>

### <span data-ttu-id="4b6a2-110">Przykład 2.Usuwanie wszystkich aktywnych certyfikatów</span><span class="sxs-lookup"><span data-stu-id="4b6a2-110">Example 2:Remove all active certificates</span></span>
```
PS C:\>Get-AzBatchCertificate -Filter "state eq 'active'" -BatchContext $Context | Remove-AzBatchCertificate -Force -BatchContext $Context
```

<span data-ttu-id="4b6a2-111">To polecenie pobiera wszystkie aktywne certyfikaty za pomocą Get-AzBatchCertificate cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b6a2-111">This command gets all certificates that are active by using the Get-AzBatchCertificate cmdlet.</span></span>
<span data-ttu-id="4b6a2-112">Polecenie przekazuje aktywne certyfikaty do bieżącego polecenia cmdlet przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="4b6a2-112">The command passes the active certificates to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4b6a2-113">To polecenie cmdlet usuwa każdy certyfikat.</span><span class="sxs-lookup"><span data-stu-id="4b6a2-113">That cmdlet removes each certificate.</span></span>
<span data-ttu-id="4b6a2-114">Polecenie określa parametr *Force.*</span><span class="sxs-lookup"><span data-stu-id="4b6a2-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="4b6a2-115">Dlatego to polecenie nie wyświetla monitu o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4b6a2-115">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="4b6a2-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b6a2-116">PARAMETERS</span></span>

### <span data-ttu-id="4b6a2-117">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="4b6a2-117">-BatchContext</span></span>
<span data-ttu-id="4b6a2-118">Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="4b6a2-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="4b6a2-119">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4b6a2-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="4b6a2-120">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="4b6a2-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="4b6a2-121">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="4b6a2-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="4b6a2-122">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="4b6a2-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="4b6a2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b6a2-123">-DefaultProfile</span></span>
<span data-ttu-id="4b6a2-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4b6a2-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b6a2-125">- Thumbprint</span><span class="sxs-lookup"><span data-stu-id="4b6a2-125">-Thumbprint</span></span>
<span data-ttu-id="4b6a2-126">Określa thumbprint certyfikatu, który usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b6a2-126">Specifies the thumbprint of the certificate that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="4b6a2-127">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="4b6a2-127">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="4b6a2-128">Określa algorytm używany do pochodzinia *parametru Thumbprint.*</span><span class="sxs-lookup"><span data-stu-id="4b6a2-128">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="4b6a2-129">Obecnie jedyną prawidłową wartością jest sha1.</span><span class="sxs-lookup"><span data-stu-id="4b6a2-129">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="4b6a2-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4b6a2-130">-Confirm</span></span>
<span data-ttu-id="4b6a2-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4b6a2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b6a2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b6a2-132">-WhatIf</span></span>
<span data-ttu-id="4b6a2-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b6a2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b6a2-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4b6a2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b6a2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b6a2-135">CommonParameters</span></span>
<span data-ttu-id="4b6a2-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b6a2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b6a2-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4b6a2-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b6a2-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4b6a2-138">INPUTS</span></span>

### <span data-ttu-id="4b6a2-139">System.String</span><span class="sxs-lookup"><span data-stu-id="4b6a2-139">System.String</span></span>

### <span data-ttu-id="4b6a2-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="4b6a2-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="4b6a2-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4b6a2-141">OUTPUTS</span></span>

### <span data-ttu-id="4b6a2-142">System.Void</span><span class="sxs-lookup"><span data-stu-id="4b6a2-142">System.Void</span></span>

## <span data-ttu-id="4b6a2-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4b6a2-143">NOTES</span></span>

## <span data-ttu-id="4b6a2-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4b6a2-144">RELATED LINKS</span></span>

[<span data-ttu-id="4b6a2-145">Get-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="4b6a2-145">Get-AzBatchCertificate</span></span>](./Get-AzBatchCertificate.md)

[<span data-ttu-id="4b6a2-146">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="4b6a2-146">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="4b6a2-147">New-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="4b6a2-147">New-AzBatchCertificate</span></span>](./New-AzBatchCertificate.md)

[<span data-ttu-id="4b6a2-148">Stop-AzBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="4b6a2-148">Stop-AzBatchCertificateDeletion</span></span>](./Stop-AzBatchCertificateDeletion.md)

[<span data-ttu-id="4b6a2-149">Polecenia cmdlet partii platformy Azure</span><span class="sxs-lookup"><span data-stu-id="4b6a2-149">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
