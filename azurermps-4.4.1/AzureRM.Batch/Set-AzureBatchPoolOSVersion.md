---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 4C3C6C81-7486-4ED6-BA30-2F202E654F77
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPoolOSVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPoolOSVersion.md
ms.openlocfilehash: 23c0a68c4b517035319150caa1d4d6a3acf799cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717876"
---
# <span data-ttu-id="a6276-101">Set-AzureBatchPoolOSVersion</span><span class="sxs-lookup"><span data-stu-id="a6276-101">Set-AzureBatchPoolOSVersion</span></span>

## <span data-ttu-id="a6276-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a6276-102">SYNOPSIS</span></span>
<span data-ttu-id="a6276-103">Umożliwia zmianę wersji systemu operacyjnego określonej puli.</span><span class="sxs-lookup"><span data-stu-id="a6276-103">Changes the operating system version of the specified pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6276-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a6276-104">SYNTAX</span></span>

```
Set-AzureBatchPoolOSVersion [-Id] <String> [-TargetOSVersion] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6276-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a6276-105">DESCRIPTION</span></span>
<span data-ttu-id="a6276-106">Polecenie cmdlet **Set-AzureBatchPoolOSVersion** umożliwia zmianę wersji systemu operacyjnego określonej puli.</span><span class="sxs-lookup"><span data-stu-id="a6276-106">The **Set-AzureBatchPoolOSVersion** cmdlet changes the operating system version of the specified pool.</span></span>

## <span data-ttu-id="a6276-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a6276-107">EXAMPLES</span></span>

### <span data-ttu-id="a6276-108">Przykład 1: Ustawianie docelowej wersji systemu operacyjnego puli</span><span class="sxs-lookup"><span data-stu-id="a6276-108">Example 1: Set the target operating system version of a pool</span></span>
```
PS C:\>Set-AzureBatchPoolOSVersion -Id "MyPool" -TargetOSVersion "WA-GUEST-OS-4.20_201505-01" -BatchContext $Context
```

<span data-ttu-id="a6276-109">To polecenie ustawia docelowy system operacyjny puli moja Pula w wersji WA-GUEST-OS-4.20 _201505-01.</span><span class="sxs-lookup"><span data-stu-id="a6276-109">This command sets the target operating system version of pool MyPool to WA-GUEST-OS-4.20_201505-01.</span></span>

## <span data-ttu-id="a6276-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a6276-110">PARAMETERS</span></span>

### <span data-ttu-id="a6276-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a6276-111">-BatchContext</span></span>
<span data-ttu-id="a6276-112">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="a6276-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a6276-113">Aby uzyskać obiekt **BatchAccountContext** , który zawiera klucze dostępu dla subskrypcji, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="a6276-113">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="a6276-114">-ID</span><span class="sxs-lookup"><span data-stu-id="a6276-114">-Id</span></span>
<span data-ttu-id="a6276-115">Określa identyfikator puli.</span><span class="sxs-lookup"><span data-stu-id="a6276-115">Specifies the ID of the pool.</span></span>

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

### <span data-ttu-id="a6276-116">-TargetOSVersion</span><span class="sxs-lookup"><span data-stu-id="a6276-116">-TargetOSVersion</span></span>
<span data-ttu-id="a6276-117">Określa wersję systemu operacyjnego gościa platformy Azure do zainstalowania na maszynach wirtualnych w puli.</span><span class="sxs-lookup"><span data-stu-id="a6276-117">Specifies the Azure Guest operating system version to install on the virtual machines in the pool.</span></span>
<span data-ttu-id="a6276-118">Aby uzyskać więcej informacji na temat wersji systemu operacyjnego gościa platformy Azure, zobacz Zestawy wersji systemu operacyjnego gościa platformy Azure oraz Matryca zgodności zestawu SDK https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ ( https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/) .</span><span class="sxs-lookup"><span data-stu-id="a6276-118">For more information on Azure Guest operating system versions, see Azure Guest OS Releases and SDK Compatibility Matrixhttps://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ (https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/).</span></span>

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

### <span data-ttu-id="a6276-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6276-119">-DefaultProfile</span></span>
<span data-ttu-id="a6276-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a6276-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6276-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6276-121">CommonParameters</span></span>
<span data-ttu-id="a6276-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6276-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6276-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6276-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6276-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a6276-124">INPUTS</span></span>

### <span data-ttu-id="a6276-125">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a6276-125">BatchAccountContext</span></span>
<span data-ttu-id="a6276-126">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="a6276-126">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="a6276-127">Ciąg</span><span class="sxs-lookup"><span data-stu-id="a6276-127">String</span></span>
<span data-ttu-id="a6276-128">Parametr "ID" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="a6276-128">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="a6276-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a6276-129">OUTPUTS</span></span>

## <span data-ttu-id="a6276-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a6276-130">NOTES</span></span>

## <span data-ttu-id="a6276-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a6276-131">RELATED LINKS</span></span>

[<span data-ttu-id="a6276-132">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="a6276-132">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)


