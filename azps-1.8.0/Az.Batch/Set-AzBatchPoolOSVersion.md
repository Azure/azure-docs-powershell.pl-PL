---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 4C3C6C81-7486-4ED6-BA30-2F202E654F77
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchpoolosversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPoolOSVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPoolOSVersion.md
ms.openlocfilehash: f35238b6236764cc3ea75132064aede71f715458
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2020
ms.locfileid: "93896910"
---
# <span data-ttu-id="9c4a3-101">Set-AzBatchPoolOSVersion</span><span class="sxs-lookup"><span data-stu-id="9c4a3-101">Set-AzBatchPoolOSVersion</span></span>

## <span data-ttu-id="9c4a3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9c4a3-102">SYNOPSIS</span></span>
<span data-ttu-id="9c4a3-103">Umożliwia zmianę wersji systemu operacyjnego określonej puli.</span><span class="sxs-lookup"><span data-stu-id="9c4a3-103">Changes the operating system version of the specified pool.</span></span>

## <span data-ttu-id="9c4a3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9c4a3-104">SYNTAX</span></span>

```
Set-AzBatchPoolOSVersion [-Id] <String> [-TargetOSVersion] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c4a3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9c4a3-105">DESCRIPTION</span></span>
<span data-ttu-id="9c4a3-106">Polecenie cmdlet **Set-AzBatchPoolOSVersion** umożliwia zmianę wersji systemu operacyjnego określonej puli.</span><span class="sxs-lookup"><span data-stu-id="9c4a3-106">The **Set-AzBatchPoolOSVersion** cmdlet changes the operating system version of the specified pool.</span></span>

## <span data-ttu-id="9c4a3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9c4a3-107">EXAMPLES</span></span>

### <span data-ttu-id="9c4a3-108">Przykład 1: Ustawianie docelowej wersji systemu operacyjnego puli</span><span class="sxs-lookup"><span data-stu-id="9c4a3-108">Example 1: Set the target operating system version of a pool</span></span>
```
PS C:\>Set-AzBatchPoolOSVersion -Id "MyPool" -TargetOSVersion "WA-GUEST-OS-4.20_201505-01" -BatchContext $Context
```

<span data-ttu-id="9c4a3-109">To polecenie ustawia docelowy system operacyjny puli moja Pula w wersji WA-GUEST-OS-4.20 _201505-01.</span><span class="sxs-lookup"><span data-stu-id="9c4a3-109">This command sets the target operating system version of pool MyPool to WA-GUEST-OS-4.20_201505-01.</span></span>

## <span data-ttu-id="9c4a3-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9c4a3-110">PARAMETERS</span></span>

### <span data-ttu-id="9c4a3-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="9c4a3-111">-BatchContext</span></span>
<span data-ttu-id="9c4a3-112">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="9c4a3-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="9c4a3-113">Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="9c4a3-113">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="9c4a3-114">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="9c4a3-114">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="9c4a3-115">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="9c4a3-115">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="9c4a3-116">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="9c4a3-116">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="9c4a3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c4a3-117">-DefaultProfile</span></span>
<span data-ttu-id="9c4a3-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9c4a3-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c4a3-119">-ID</span><span class="sxs-lookup"><span data-stu-id="9c4a3-119">-Id</span></span>
<span data-ttu-id="9c4a3-120">Określa identyfikator puli.</span><span class="sxs-lookup"><span data-stu-id="9c4a3-120">Specifies the ID of the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c4a3-121">-TargetOSVersion</span><span class="sxs-lookup"><span data-stu-id="9c4a3-121">-TargetOSVersion</span></span>
<span data-ttu-id="9c4a3-122">Określa wersję systemu operacyjnego gościa platformy Azure do zainstalowania na maszynach wirtualnych w puli.</span><span class="sxs-lookup"><span data-stu-id="9c4a3-122">Specifies the Azure Guest operating system version to install on the virtual machines in the pool.</span></span>
<span data-ttu-id="9c4a3-123">Aby uzyskać więcej informacji na temat wersji systemu operacyjnego gościa platformy Azure, zobacz Zestawy wersji systemu operacyjnego gościa platformy Azure oraz Matryca zgodności zestawu SDK https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ ( https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/) .</span><span class="sxs-lookup"><span data-stu-id="9c4a3-123">For more information on Azure Guest operating system versions, see Azure Guest OS Releases and SDK Compatibility Matrixhttps://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ (https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c4a3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c4a3-124">CommonParameters</span></span>
<span data-ttu-id="9c4a3-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c4a3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c4a3-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c4a3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c4a3-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9c4a3-127">INPUTS</span></span>

### <span data-ttu-id="9c4a3-128">System. String</span><span class="sxs-lookup"><span data-stu-id="9c4a3-128">System.String</span></span>

### <span data-ttu-id="9c4a3-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="9c4a3-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="9c4a3-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9c4a3-130">OUTPUTS</span></span>

### <span data-ttu-id="9c4a3-131">System. void</span><span class="sxs-lookup"><span data-stu-id="9c4a3-131">System.Void</span></span>

## <span data-ttu-id="9c4a3-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9c4a3-132">NOTES</span></span>

## <span data-ttu-id="9c4a3-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9c4a3-133">RELATED LINKS</span></span>

[<span data-ttu-id="9c4a3-134">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="9c4a3-134">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)


