---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A9C98F8F-90F2-4BF4-A234-31966FBB975B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchCertificate.md
ms.openlocfilehash: c78cf87d4e68c4a9e1b896235d85dde9e8458f1e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547588"
---
# <span data-ttu-id="0f9f2-101">Get-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="0f9f2-101">Get-AzureBatchCertificate</span></span>

## <span data-ttu-id="0f9f2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0f9f2-102">SYNOPSIS</span></span>
<span data-ttu-id="0f9f2-103">Pobiera certyfikaty na koncie wsadowym.</span><span class="sxs-lookup"><span data-stu-id="0f9f2-103">Gets the certificates in a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f9f2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0f9f2-104">SYNTAX</span></span>

### <span data-ttu-id="0f9f2-105">ODataFilter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0f9f2-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchCertificate [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f9f2-106">Mając</span><span class="sxs-lookup"><span data-stu-id="0f9f2-106">Thumbprint</span></span>
```
Get-AzureBatchCertificate [-ThumbprintAlgorithm] <String> [-Thumbprint] <String> [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f9f2-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0f9f2-107">DESCRIPTION</span></span>
<span data-ttu-id="0f9f2-108">Polecenie cmdlet **Get-AzureBatchCertificate** pobiera certyfikaty na koncie usługi Azure Batch, które określa parametr *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="0f9f2-108">The **Get-AzureBatchCertificate** cmdlet gets the certificates in the Azure Batch account that the *BatchContext* parameter specifies.</span></span>
<span data-ttu-id="0f9f2-109">Aby uzyskać określony certyfikat, określ parametry *ThumbprintAlgorithm* i *odcisk palca* .</span><span class="sxs-lookup"><span data-stu-id="0f9f2-109">To obtain a particular certificate, specify the *ThumbprintAlgorithm* and *Thumbprint* parameters.</span></span>
<span data-ttu-id="0f9f2-110">Określ parametr *Filter* , aby uzyskać certyfikaty zgodne z filtrem Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="0f9f2-110">Specify the *Filter* parameter to get the certificates that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="0f9f2-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0f9f2-111">EXAMPLES</span></span>

### <span data-ttu-id="0f9f2-112">Przykład 1: uzyskiwanie certyfikatu według odcisku palca</span><span class="sxs-lookup"><span data-stu-id="0f9f2-112">Example 1: Get a certificate by thumbprint</span></span>
```
PS C:\>Get-AzureBatchCertificate -ThumbprintAlgorithm "sha1" - Thumbprint "C1E494A415149C5F211C4778B52F2E834A07247C" -BatchContext $Context
Thumbprint                  : c1e494a415149c5f211c4778b52f2e834a07247c
ThumbprintAlgorithm         : sha1
Url                         : https://pstests.eastus.batch.azure.com/certificates(thumbprintAlgorithm=sha1,thumbprint=C1E494A415149C5F211C4778B52F2E834A07247
C) 
State                       : Active
StateTransitionTime         : 10/6/2015 6:21:16 PM
PreviousState               : 
PreviousStateTransitionTime : 
Data                        : 
CertificateFormat           : 
Password                    : 
PublicData                  : MIIB9DCCAWGgAwIBAgIQpUXhwCuAPJRDhl7kY/0PdTAJBgUrDgMCHQUAMBYxFDASBgNVBAMTC0JhdGNoVGVzdDAxMB4XDTE1MTAwMjE2MjkwNVoXDTM5MTIzMTIzNTk
1OVowFjEUMBIGA1UEAxMLQmF0Y2hUZXN0MDEwgZ8wDQYJKoZIhvcNAQEBBQADgY0AMIGJAoGBAM06unpRipn3BmHBM75d0s8w/Wwifci16PoJo4c2V68GwsCCFsNOn5
ypo7BBXo1fpBjrnso5w+koaE5LjxkBSVm+TkogwbKlW6WURTM0O5viRVbPnEEU/Y01Pj5cJElFuLEk9Uoe/r/lP8b5A607t1cPjSXkwhEZEYc3LkHDSo0ZAgMBAAGjS
zBJMEcGA1UdAQRAMD6AEFRsTAsrvF+FmPuICooZXaKhGDAWMRQwEgYDVQQDEwtCYXRjaFRlc3QwMYIQpUXhwCuAPJRDhl7kY/0PdTAJBgUrDgMCHQUAA4GBALt0F8Ep
+8XVE/M2aNtxzlku72gxiOiAo1HmpUaixXx3gl8kdP3xgoKMaq4JskqdLmbJJUnCQ3wmzsdPwjswsW2ycT12zuBddaiS+id98k8U/KYc6FxMgS+H70FYOxARLn7P4FS
SBf/QCyign+BherzezdZ5NBdfzbmWxIMP5iFJ
DeleteCertificateError      :
```

<span data-ttu-id="0f9f2-113">To polecenie pobiera jeden certyfikat z określonym palcem.</span><span class="sxs-lookup"><span data-stu-id="0f9f2-113">This command gets a single certificate that has the specified thumbprint.</span></span>
<span data-ttu-id="0f9f2-114">Algorytm odcisku palca certyfikatu to SHA1.</span><span class="sxs-lookup"><span data-stu-id="0f9f2-114">The certificate thumbprint algorithm is sha1.</span></span>

### <span data-ttu-id="0f9f2-115">Przykład 2: uzyskiwanie przefiltrowanych certyfikatów</span><span class="sxs-lookup"><span data-stu-id="0f9f2-115">Example 2: Get filtered certificates</span></span>
```
PS C:\>Get-AzureBatchCertificate -Filter "state eq 'active'" -BatchContext $Context
Thumbprint                  : 025b351b087a084c5067f5e71eff8591970323f9
ThumbprintAlgorithm         : sha1
Url                         : https://pstests.eastus.batch.azure.com/certificates(thumbprintAlgorithm=sha1,thumbprint=025b351b087a084c5067f5e71eff8591970323f9) 
State                       : Active
StateTransitionTime         : 10/6/2015 6:21:17 PM
PreviousState               : 
PreviousStateTransitionTime : 
Data                        : 
CertificateFormat           : 
Password                    : 
PublicData                  : MIIB9DCCAWGgAwIBAgIQy9W5y8iwhppGhtAG06dHKTAJBgUrDgMCHQUAMBYxFDASBgNVBAMTC0JhdGNoVGVzdDAyMB4XDTE1MTAwMjE2MjkxNFoXDTM5MTIzMTIzNTk
1OVowFjEUMBIGA1UEAxMLQmF0Y2hUZXN0MDIwgZ8wDQYJKoZIhvcNAQEBBQADgY0AMIGJAoGBAJxagvVrlnKfv6hfzSiFJUkdGkPjC3tFiKebK6IaeHzesFdFfupXUE
wT0xOWh9xwa3OVkPECEc/u1sw3iVX/J4AODiwzmOWutoVRpWjxGFpgw9+dPvXMjs/Ue7JL7ag3siHs5EcarW91qKbgtko6i/r4emaRyk60U93TrbWQAWJ9AgMBAAGjS
zBJMEcGA1UdAQRAMD6AEAdqsOpyeXF/uDe7ZGKeez+hGDAWMRQwEgYDVQQDEwtCYXRjaFRlc3QwMoIQy9W5y8iwhppGhtAG06dHKTAJBgUrDgMCHQUAA4GBAC0MaAem
6ByyURFvGnFZyjEepjXC5wcaGq+gguDFe8rG88ceig1ZqewdcmC1y4p05uBhbmETbYVWzJarNsHYq2LTihi4t2J4jt2YVYz/IRdUB82iaFFbJRSPrN+6xD3KM2lve5N
4OjtlZAdiXiSUYFf3I6ypberUsAdba3QQajCN
DeleteCertificateError      : 

Thumbprint                  : c1e494a415149c5f211c4778b52f2e834a07247c
ThumbprintAlgorithm         : sha1
Url                         : https://pstests.eastus.batch.azure.com/certificates(thumbprintAlgorithm=sha1,thumbprint=c1e494a415149c5f211c4778b52f2e834a07247c) 
State                       : Active
StateTransitionTime         : 10/6/2015 6:21:16 PM
PreviousState               : 
PreviousStateTransitionTime : 
Data                        : 
CertificateFormat           : 
Password                    : 
PublicData                  : MIIB9DCCAWGgAwIBAgIQpUXhwCuAPJRDhl7kY/0PdTAJBgUrDgMCHQUAMBYxFDASBgNVBAMTC0JhdGNoVGVzdDAxMB4XDTE1MTAwMjE2MjkwNVoXDTM5MTIzMTIzNTk
1OVowFjEUMBIGA1UEAxMLQmF0Y2hUZXN0MDEwgZ8wDQYJKoZIhvcNAQEBBQADgY0AMIGJAoGBAM06unpRipn3BmHBM75d0s8w/Wwifci16PoJo4c2V68GwsCCFsNOn5
ypo7BBXo1fpBjrnso5w+koaE5LjxkBSVm+TkogwbKlW6WURTM0O5viRVbPnEEU/Y01Pj5cJElFuLEk9Uoe/r/lP8b5A607t1cPjSXkwhEZEYc3LkHDSo0ZAgMBAAGjS
zBJMEcGA1UdAQRAMD6AEFRsTAsrvF+FmPuICooZXaKhGDAWMRQwEgYDVQQDEwtCYXRjaFRlc3QwMYIQpUXhwCuAPJRDhl7kY/0PdTAJBgUrDgMCHQUAA4GBALt0F8Ep
+8XVE/M2aNtxzlku72gxiOiAo1HmpUaixXx3gl8kdP3xgoKMaq4JskqdLmbJJUnCQ3wmzsdPwjswsW2ycT12zuBddaiS+id98k8U/KYc6FxMgS+H70FYOxARLn7P4FS
SBf/QCyign+BherzezdZ5NBdfzbmWxIMP5iFJ
DeleteCertificateError      :
```

<span data-ttu-id="0f9f2-116">To polecenie pobiera wszystkie certyfikaty w stanie aktywnym z konta wsadowego.</span><span class="sxs-lookup"><span data-stu-id="0f9f2-116">This command gets all certificates in the active state from the Batch account.</span></span>
<span data-ttu-id="0f9f2-117">Parametr *Filter* określa stan.</span><span class="sxs-lookup"><span data-stu-id="0f9f2-117">The *Filter* parameter specifies the state.</span></span>

## <span data-ttu-id="0f9f2-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0f9f2-118">PARAMETERS</span></span>

### <span data-ttu-id="0f9f2-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="0f9f2-119">-BatchContext</span></span>
<span data-ttu-id="0f9f2-120">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="0f9f2-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="0f9f2-121">Jeśli używasz polecenia cmdlet Get-AzureRmBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="0f9f2-121">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="0f9f2-122">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="0f9f2-122">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="0f9f2-123">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="0f9f2-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="0f9f2-124">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="0f9f2-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="0f9f2-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f9f2-125">-DefaultProfile</span></span>
<span data-ttu-id="0f9f2-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0f9f2-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f9f2-127">-Filter</span><span class="sxs-lookup"><span data-stu-id="0f9f2-127">-Filter</span></span>
<span data-ttu-id="0f9f2-128">Określa klauzulę filtru OData.</span><span class="sxs-lookup"><span data-stu-id="0f9f2-128">Specifies an OData filter clause.</span></span>
<span data-ttu-id="0f9f2-129">Jeśli określisz ten parametr, to polecenie cmdlet otrzyma certyfikaty zgodne z filtrem.</span><span class="sxs-lookup"><span data-stu-id="0f9f2-129">If you specify this parameter, this cmdlet gets the certificates that match the filter.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f9f2-130">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="0f9f2-130">-MaxCount</span></span>
<span data-ttu-id="0f9f2-131">Określa maksymalną liczbę zwracanych certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="0f9f2-131">Specifies the maximum number of certificates to return.</span></span>
<span data-ttu-id="0f9f2-132">Jeśli określisz wartość zero (0) lub mniejszą, polecenie cmdlet nie używa górnego limitu.</span><span class="sxs-lookup"><span data-stu-id="0f9f2-132">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="0f9f2-133">Wartość domyślna to 1000.</span><span class="sxs-lookup"><span data-stu-id="0f9f2-133">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f9f2-134">-Wybierz pozycję</span><span class="sxs-lookup"><span data-stu-id="0f9f2-134">-Select</span></span>
<span data-ttu-id="0f9f2-135">Określa klauzulę SELECT OData.</span><span class="sxs-lookup"><span data-stu-id="0f9f2-135">Specifies an OData select clause.</span></span>
<span data-ttu-id="0f9f2-136">Określ wartość dla tego parametru, aby uzyskać określone właściwości, a nie wszystkie właściwości obiektu.</span><span class="sxs-lookup"><span data-stu-id="0f9f2-136">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="0f9f2-137">-Odcisk palca</span><span class="sxs-lookup"><span data-stu-id="0f9f2-137">-Thumbprint</span></span>
<span data-ttu-id="0f9f2-138">Określa odcisk palca certyfikatu, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f9f2-138">Specifies the thumbprint of the certificate that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: Thumbprint
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f9f2-139">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="0f9f2-139">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="0f9f2-140">Określa algorytm używany do uzyskania parametru *odcisku palca* .</span><span class="sxs-lookup"><span data-stu-id="0f9f2-140">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="0f9f2-141">Obecnie jedyną prawidłową wartością jest SHA1.</span><span class="sxs-lookup"><span data-stu-id="0f9f2-141">Currently, the only valid value is sha1.</span></span>

```yaml
Type: System.String
Parameter Sets: Thumbprint
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f9f2-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f9f2-142">CommonParameters</span></span>
<span data-ttu-id="0f9f2-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f9f2-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f9f2-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f9f2-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f9f2-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0f9f2-145">INPUTS</span></span>

### <span data-ttu-id="0f9f2-146">System. String</span><span class="sxs-lookup"><span data-stu-id="0f9f2-146">System.String</span></span>

### <span data-ttu-id="0f9f2-147">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="0f9f2-147">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="0f9f2-148">Parametry: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0f9f2-148">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="0f9f2-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0f9f2-149">OUTPUTS</span></span>

### <span data-ttu-id="0f9f2-150">Microsoft.Azure.Commands.Batch. Modele. PSCertificate</span><span class="sxs-lookup"><span data-stu-id="0f9f2-150">Microsoft.Azure.Commands.Batch.Models.PSCertificate</span></span>

## <span data-ttu-id="0f9f2-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0f9f2-151">NOTES</span></span>

## <span data-ttu-id="0f9f2-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0f9f2-152">RELATED LINKS</span></span>

[<span data-ttu-id="0f9f2-153">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="0f9f2-153">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="0f9f2-154">Nowe — AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="0f9f2-154">New-AzureBatchCertificate</span></span>](./New-AzureBatchCertificate.md)

[<span data-ttu-id="0f9f2-155">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="0f9f2-155">Remove-AzureBatchCertificate</span></span>](./Remove-AzureBatchCertificate.md)

[<span data-ttu-id="0f9f2-156">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="0f9f2-156">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)

