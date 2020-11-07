---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 4C3C6C81-7486-4ED6-BA30-2F202E654F77
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchpoolosversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPoolOSVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPoolOSVersion.md
ms.openlocfilehash: cd21c9ce84a96ada003eb6520c9a2a115df186cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552224"
---
# <span data-ttu-id="6f0e5-101">Set-AzureBatchPoolOSVersion</span><span class="sxs-lookup"><span data-stu-id="6f0e5-101">Set-AzureBatchPoolOSVersion</span></span>

## <span data-ttu-id="6f0e5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6f0e5-102">SYNOPSIS</span></span>
<span data-ttu-id="6f0e5-103">Umożliwia zmianę wersji systemu operacyjnego określonej puli.</span><span class="sxs-lookup"><span data-stu-id="6f0e5-103">Changes the operating system version of the specified pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f0e5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6f0e5-104">SYNTAX</span></span>

```
Set-AzureBatchPoolOSVersion [-Id] <String> [-TargetOSVersion] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f0e5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6f0e5-105">DESCRIPTION</span></span>
<span data-ttu-id="6f0e5-106">Polecenie cmdlet **Set-AzureBatchPoolOSVersion** umożliwia zmianę wersji systemu operacyjnego określonej puli.</span><span class="sxs-lookup"><span data-stu-id="6f0e5-106">The **Set-AzureBatchPoolOSVersion** cmdlet changes the operating system version of the specified pool.</span></span>

## <span data-ttu-id="6f0e5-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6f0e5-107">EXAMPLES</span></span>

### <span data-ttu-id="6f0e5-108">Przykład 1: Ustawianie docelowej wersji systemu operacyjnego puli</span><span class="sxs-lookup"><span data-stu-id="6f0e5-108">Example 1: Set the target operating system version of a pool</span></span>
```
PS C:\>Set-AzureBatchPoolOSVersion -Id "MyPool" -TargetOSVersion "WA-GUEST-OS-4.20_201505-01" -BatchContext $Context
```

<span data-ttu-id="6f0e5-109">To polecenie ustawia docelowy system operacyjny puli moja Pula w wersji WA-GUEST-OS-4.20 _201505-01.</span><span class="sxs-lookup"><span data-stu-id="6f0e5-109">This command sets the target operating system version of pool MyPool to WA-GUEST-OS-4.20_201505-01.</span></span>

## <span data-ttu-id="6f0e5-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6f0e5-110">PARAMETERS</span></span>

### <span data-ttu-id="6f0e5-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="6f0e5-111">-BatchContext</span></span>
<span data-ttu-id="6f0e5-112">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="6f0e5-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6f0e5-113">Jeśli używasz polecenia cmdlet Get-AzureRmBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="6f0e5-113">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="6f0e5-114">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="6f0e5-114">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="6f0e5-115">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="6f0e5-115">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="6f0e5-116">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="6f0e5-116">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="6f0e5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f0e5-117">-DefaultProfile</span></span>
<span data-ttu-id="6f0e5-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6f0e5-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f0e5-119">-ID</span><span class="sxs-lookup"><span data-stu-id="6f0e5-119">-Id</span></span>
<span data-ttu-id="6f0e5-120">Określa identyfikator puli.</span><span class="sxs-lookup"><span data-stu-id="6f0e5-120">Specifies the ID of the pool.</span></span>

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

### <span data-ttu-id="6f0e5-121">-TargetOSVersion</span><span class="sxs-lookup"><span data-stu-id="6f0e5-121">-TargetOSVersion</span></span>
<span data-ttu-id="6f0e5-122">Określa wersję systemu operacyjnego gościa platformy Azure do zainstalowania na maszynach wirtualnych w puli.</span><span class="sxs-lookup"><span data-stu-id="6f0e5-122">Specifies the Azure Guest operating system version to install on the virtual machines in the pool.</span></span>
<span data-ttu-id="6f0e5-123">Aby uzyskać więcej informacji na temat wersji systemu operacyjnego gościa platformy Azure, zobacz Zestawy wersji systemu operacyjnego gościa platformy Azure oraz Matryca zgodności zestawu SDK https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ ( https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/) .</span><span class="sxs-lookup"><span data-stu-id="6f0e5-123">For more information on Azure Guest operating system versions, see Azure Guest OS Releases and SDK Compatibility Matrixhttps://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ (https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f0e5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f0e5-124">CommonParameters</span></span>
<span data-ttu-id="6f0e5-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f0e5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f0e5-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f0e5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f0e5-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6f0e5-127">INPUTS</span></span>

### <span data-ttu-id="6f0e5-128">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6f0e5-128">BatchAccountContext</span></span>
<span data-ttu-id="6f0e5-129">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="6f0e5-129">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="6f0e5-130">Ciąg</span><span class="sxs-lookup"><span data-stu-id="6f0e5-130">String</span></span>
<span data-ttu-id="6f0e5-131">Parametr "ID" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="6f0e5-131">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="6f0e5-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6f0e5-132">OUTPUTS</span></span>

## <span data-ttu-id="6f0e5-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6f0e5-133">NOTES</span></span>

## <span data-ttu-id="6f0e5-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6f0e5-134">RELATED LINKS</span></span>

[<span data-ttu-id="6f0e5-135">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="6f0e5-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

