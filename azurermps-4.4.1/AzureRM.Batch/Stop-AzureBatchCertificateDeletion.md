---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B3C8A2DB-6571-418D-8C4B-3BE3FDA42F89
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchCertificateDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchCertificateDeletion.md
ms.openlocfilehash: 820e94b75c19d49f4e49ee8419f7807a839f925b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548352"
---
# <span data-ttu-id="f84a1-101">Stop-AzureBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="f84a1-101">Stop-AzureBatchCertificateDeletion</span></span>

## <span data-ttu-id="f84a1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f84a1-102">SYNOPSIS</span></span>
<span data-ttu-id="f84a1-103">Anuluje nieudaną operację usunięcia certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="f84a1-103">Cancels a failed deletion of a certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f84a1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f84a1-104">SYNTAX</span></span>

```
Stop-AzureBatchCertificateDeletion [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f84a1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f84a1-105">DESCRIPTION</span></span>
<span data-ttu-id="f84a1-106">Polecenie cmdlet **stop-AzureBatchCertificateDeletion** anuluje usunięcie nieudanego certyfikatu w usłudze Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="f84a1-106">The **Stop-AzureBatchCertificateDeletion** cmdlet cancels a failed deletion of a certificate in the Azure Batch service.</span></span>
<span data-ttu-id="f84a1-107">Możesz zatrzymać usuwanie tylko wtedy, gdy certyfikat jest w stanie **DeleteFailed** .</span><span class="sxs-lookup"><span data-stu-id="f84a1-107">You can stop a deletion only if the certificate is in the **DeleteFailed** state.</span></span>
<span data-ttu-id="f84a1-108">Ta cmldet przywraca stan **aktywny** .</span><span class="sxs-lookup"><span data-stu-id="f84a1-108">This cmldet restores the certificate to the **Active** state.</span></span>

## <span data-ttu-id="f84a1-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f84a1-109">EXAMPLES</span></span>

### <span data-ttu-id="f84a1-110">Przykład 1. Anulowanie usunięcia</span><span class="sxs-lookup"><span data-stu-id="f84a1-110">Example 1: Cancel a deletion</span></span>
```
PS C:\>Stop-AzureBatchCertificateDeletion -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="f84a1-111">To polecenie anuluje usunięcie certyfikatu o określonym odcisku palca.</span><span class="sxs-lookup"><span data-stu-id="f84a1-111">This command cancels the deletion of the certificate that has the specified thumbprint.</span></span>

## <span data-ttu-id="f84a1-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f84a1-112">PARAMETERS</span></span>

### <span data-ttu-id="f84a1-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f84a1-113">-BatchContext</span></span>
<span data-ttu-id="f84a1-114">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="f84a1-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f84a1-115">Aby uzyskać obiekt **BatchAccountContext** , który zawiera klucze dostępu dla subskrypcji, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="f84a1-115">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="f84a1-116">-Odcisk palca</span><span class="sxs-lookup"><span data-stu-id="f84a1-116">-Thumbprint</span></span>
<span data-ttu-id="f84a1-117">Określa odcisk palca certyfikatu, który jest przywracany do stanu **aktywnego** .</span><span class="sxs-lookup"><span data-stu-id="f84a1-117">Specifies the thumbprint of the certificate that this cmdlet restores to the **Active** state.</span></span>

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

### <span data-ttu-id="f84a1-118">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="f84a1-118">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="f84a1-119">Określa algorytm używany do uzyskania parametru *odcisku palca* .</span><span class="sxs-lookup"><span data-stu-id="f84a1-119">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="f84a1-120">Obecnie jedyną prawidłową wartością jest SHA1.</span><span class="sxs-lookup"><span data-stu-id="f84a1-120">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="f84a1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f84a1-121">-DefaultProfile</span></span>
<span data-ttu-id="f84a1-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f84a1-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f84a1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f84a1-123">CommonParameters</span></span>
<span data-ttu-id="f84a1-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f84a1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f84a1-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f84a1-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f84a1-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f84a1-126">INPUTS</span></span>

### <span data-ttu-id="f84a1-127">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f84a1-127">BatchAccountContext</span></span>
<span data-ttu-id="f84a1-128">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="f84a1-128">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="f84a1-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f84a1-129">OUTPUTS</span></span>

## <span data-ttu-id="f84a1-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f84a1-130">NOTES</span></span>

## <span data-ttu-id="f84a1-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f84a1-131">RELATED LINKS</span></span>

[<span data-ttu-id="f84a1-132">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="f84a1-132">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="f84a1-133">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="f84a1-133">Remove-AzureBatchCertificate</span></span>](./Remove-AzureBatchCertificate.md)

[<span data-ttu-id="f84a1-134">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="f84a1-134">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


