---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B3C8A2DB-6571-418D-8C4B-3BE3FDA42F89
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchcertificatedeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchCertificateDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchCertificateDeletion.md
ms.openlocfilehash: 39b37f6f81a849e7ea3fc59dde6c99bebc3bfd1d
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2020
ms.locfileid: "94061708"
---
# <span data-ttu-id="d5a68-101">Stop-AzBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="d5a68-101">Stop-AzBatchCertificateDeletion</span></span>

## <span data-ttu-id="d5a68-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d5a68-102">SYNOPSIS</span></span>
<span data-ttu-id="d5a68-103">Anuluje nieudaną operację usunięcia certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="d5a68-103">Cancels a failed deletion of a certificate.</span></span>

## <span data-ttu-id="d5a68-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d5a68-104">SYNTAX</span></span>

```
Stop-AzBatchCertificateDeletion [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5a68-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d5a68-105">DESCRIPTION</span></span>
<span data-ttu-id="d5a68-106">Polecenie cmdlet **stop-AzBatchCertificateDeletion** anuluje usunięcie nieudanego certyfikatu w usłudze Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="d5a68-106">The **Stop-AzBatchCertificateDeletion** cmdlet cancels a failed deletion of a certificate in the Azure Batch service.</span></span>
<span data-ttu-id="d5a68-107">Możesz zatrzymać usuwanie tylko wtedy, gdy certyfikat jest w stanie **DeleteFailed** .</span><span class="sxs-lookup"><span data-stu-id="d5a68-107">You can stop a deletion only if the certificate is in the **DeleteFailed** state.</span></span>
<span data-ttu-id="d5a68-108">To polecenie cmdlet przywraca stan **aktywny** .</span><span class="sxs-lookup"><span data-stu-id="d5a68-108">This cmdlet restores the certificate to the **Active** state.</span></span>

## <span data-ttu-id="d5a68-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d5a68-109">EXAMPLES</span></span>

### <span data-ttu-id="d5a68-110">Przykład 1. Anulowanie usunięcia</span><span class="sxs-lookup"><span data-stu-id="d5a68-110">Example 1: Cancel a deletion</span></span>
```
PS C:\>Stop-AzBatchCertificateDeletion -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="d5a68-111">To polecenie anuluje usunięcie certyfikatu o określonym odcisku palca.</span><span class="sxs-lookup"><span data-stu-id="d5a68-111">This command cancels the deletion of the certificate that has the specified thumbprint.</span></span>

## <span data-ttu-id="d5a68-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d5a68-112">PARAMETERS</span></span>

### <span data-ttu-id="d5a68-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d5a68-113">-BatchContext</span></span>
<span data-ttu-id="d5a68-114">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="d5a68-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d5a68-115">Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="d5a68-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="d5a68-116">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKey, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="d5a68-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="d5a68-117">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="d5a68-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="d5a68-118">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="d5a68-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="d5a68-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5a68-119">-DefaultProfile</span></span>
<span data-ttu-id="d5a68-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d5a68-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5a68-121">-Odcisk palca</span><span class="sxs-lookup"><span data-stu-id="d5a68-121">-Thumbprint</span></span>
<span data-ttu-id="d5a68-122">Określa odcisk palca certyfikatu, który jest przywracany do stanu **aktywnego** .</span><span class="sxs-lookup"><span data-stu-id="d5a68-122">Specifies the thumbprint of the certificate that this cmdlet restores to the **Active** state.</span></span>

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

### <span data-ttu-id="d5a68-123">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="d5a68-123">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="d5a68-124">Określa algorytm używany do uzyskania parametru *odcisku palca* .</span><span class="sxs-lookup"><span data-stu-id="d5a68-124">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="d5a68-125">Obecnie jedyną prawidłową wartością jest SHA1.</span><span class="sxs-lookup"><span data-stu-id="d5a68-125">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="d5a68-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5a68-126">CommonParameters</span></span>
<span data-ttu-id="d5a68-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5a68-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5a68-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d5a68-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5a68-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d5a68-129">INPUTS</span></span>

### <span data-ttu-id="d5a68-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d5a68-130">System.String</span></span>

### <span data-ttu-id="d5a68-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d5a68-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="d5a68-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d5a68-132">OUTPUTS</span></span>

### <span data-ttu-id="d5a68-133">System. void</span><span class="sxs-lookup"><span data-stu-id="d5a68-133">System.Void</span></span>

## <span data-ttu-id="d5a68-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d5a68-134">NOTES</span></span>

## <span data-ttu-id="d5a68-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d5a68-135">RELATED LINKS</span></span>

[<span data-ttu-id="d5a68-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="d5a68-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="d5a68-137">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="d5a68-137">Remove-AzBatchCertificate</span></span>](./Remove-AzBatchCertificate.md)

[<span data-ttu-id="d5a68-138">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="d5a68-138">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


