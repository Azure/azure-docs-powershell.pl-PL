---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B3C8A2DB-6571-418D-8C4B-3BE3FDA42F89
online version: https://docs.microsoft.com/powershell/module/az.batch/stop-azbatchcertificatedeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchCertificateDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchCertificateDeletion.md
ms.openlocfilehash: 099f6a1ea19e9810745715dbc90ea0e0b1962285
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994505"
---
# <span data-ttu-id="79be6-101">Stop-AzBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="79be6-101">Stop-AzBatchCertificateDeletion</span></span>

## <span data-ttu-id="79be6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79be6-102">SYNOPSIS</span></span>
<span data-ttu-id="79be6-103">Anulowanie nieudane usunięcie certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="79be6-103">Cancels a failed deletion of a certificate.</span></span>

## <span data-ttu-id="79be6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="79be6-104">SYNTAX</span></span>

```
Stop-AzBatchCertificateDeletion [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79be6-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="79be6-105">DESCRIPTION</span></span>
<span data-ttu-id="79be6-106">Polecenie **cmdlet Stop-AzBatchCertificateDeletion anuluje** nieudane usunięcie certyfikatu w usłudze wsadowej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="79be6-106">The **Stop-AzBatchCertificateDeletion** cmdlet cancels a failed deletion of a certificate in the Azure Batch service.</span></span>
<span data-ttu-id="79be6-107">Usuwanie można zatrzymać tylko wtedy, gdy certyfikat znajduje się w stanie **DeleteFailed.**</span><span class="sxs-lookup"><span data-stu-id="79be6-107">You can stop a deletion only if the certificate is in the **DeleteFailed** state.</span></span>
<span data-ttu-id="79be6-108">To polecenie cmdlet przywraca certyfikat do stanu **Aktywnego.**</span><span class="sxs-lookup"><span data-stu-id="79be6-108">This cmdlet restores the certificate to the **Active** state.</span></span>

## <span data-ttu-id="79be6-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="79be6-109">EXAMPLES</span></span>

### <span data-ttu-id="79be6-110">Przykład 1. Anulowanie usunięcia</span><span class="sxs-lookup"><span data-stu-id="79be6-110">Example 1: Cancel a deletion</span></span>
```
PS C:\>Stop-AzBatchCertificateDeletion -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="79be6-111">To polecenie anuluje usunięcie certyfikatu z określonym znakiem usbprint.</span><span class="sxs-lookup"><span data-stu-id="79be6-111">This command cancels the deletion of the certificate that has the specified thumbprint.</span></span>

## <span data-ttu-id="79be6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79be6-112">PARAMETERS</span></span>

### <span data-ttu-id="79be6-113">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="79be6-113">-BatchContext</span></span>
<span data-ttu-id="79be6-114">Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="79be6-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="79be6-115">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="79be6-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="79be6-116">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="79be6-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="79be6-117">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="79be6-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="79be6-118">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="79be6-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="79be6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79be6-119">-DefaultProfile</span></span>
<span data-ttu-id="79be6-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="79be6-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79be6-121">- Thumbprint</span><span class="sxs-lookup"><span data-stu-id="79be6-121">-Thumbprint</span></span>
<span data-ttu-id="79be6-122">Określa thumbprint certyfikatu, który to polecenie cmdlet przywraca do **stanu Aktywnego.**</span><span class="sxs-lookup"><span data-stu-id="79be6-122">Specifies the thumbprint of the certificate that this cmdlet restores to the **Active** state.</span></span>

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

### <span data-ttu-id="79be6-123">- ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="79be6-123">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="79be6-124">Określa algorytm używany do pochodzinia *parametru Thumbprint.*</span><span class="sxs-lookup"><span data-stu-id="79be6-124">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="79be6-125">Obecnie jedyną prawidłową wartością jest sha1.</span><span class="sxs-lookup"><span data-stu-id="79be6-125">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="79be6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79be6-126">CommonParameters</span></span>
<span data-ttu-id="79be6-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79be6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79be6-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="79be6-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79be6-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79be6-129">INPUTS</span></span>

### <span data-ttu-id="79be6-130">System.String</span><span class="sxs-lookup"><span data-stu-id="79be6-130">System.String</span></span>

### <span data-ttu-id="79be6-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="79be6-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="79be6-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79be6-132">OUTPUTS</span></span>

### <span data-ttu-id="79be6-133">System.Void</span><span class="sxs-lookup"><span data-stu-id="79be6-133">System.Void</span></span>

## <span data-ttu-id="79be6-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="79be6-134">NOTES</span></span>

## <span data-ttu-id="79be6-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="79be6-135">RELATED LINKS</span></span>

[<span data-ttu-id="79be6-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="79be6-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="79be6-137">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="79be6-137">Remove-AzBatchCertificate</span></span>](./Remove-AzBatchCertificate.md)

[<span data-ttu-id="79be6-138">Polecenia cmdlet partii platformy Azure</span><span class="sxs-lookup"><span data-stu-id="79be6-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
