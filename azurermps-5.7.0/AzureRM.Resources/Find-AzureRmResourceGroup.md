---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: EFBBFB60-D972-47B8-997E-B737F0CA007E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/find-azurermresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResourceGroup.md
ms.openlocfilehash: 42e268a36cf6ea45d4a36ef1a7c3edd825c6e8ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548023"
---
# <span data-ttu-id="38396-101">Find-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="38396-101">Find-AzureRmResourceGroup</span></span>

## <span data-ttu-id="38396-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="38396-102">SYNOPSIS</span></span>
<span data-ttu-id="38396-103">Umożliwia wyszukiwanie grup zasobów.</span><span class="sxs-lookup"><span data-stu-id="38396-103">Searches for resource groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38396-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="38396-104">SYNTAX</span></span>

```
Find-AzureRmResourceGroup [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38396-105">Opis</span><span class="sxs-lookup"><span data-stu-id="38396-105">DESCRIPTION</span></span>
<span data-ttu-id="38396-106">Polecenie cmdlet **Find-AzureRmResourceGroup** umożliwia wyszukiwanie grup zasobów przy użyciu określonych parametrów.</span><span class="sxs-lookup"><span data-stu-id="38396-106">The **Find-AzureRmResourceGroup** cmdlet searches for resource groups using the specified parameters.</span></span>

## <span data-ttu-id="38396-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="38396-107">EXAMPLES</span></span>

### <span data-ttu-id="38396-108">Przykład 1: Znajdowanie wszystkich grup zasobów</span><span class="sxs-lookup"><span data-stu-id="38396-108">Example 1: Find all resource groups</span></span>
```
PS C:\>Find-AzureRmResourceGroup
```

<span data-ttu-id="38396-109">To polecenie umożliwia znalezienie wszystkich grup zasobów.</span><span class="sxs-lookup"><span data-stu-id="38396-109">This command finds all resource groups.</span></span>

### <span data-ttu-id="38396-110">Przykład 2: Znajdowanie grup zasobów według nazwy tagu</span><span class="sxs-lookup"><span data-stu-id="38396-110">Example 2: Find resource groups by tag name</span></span>
```
PS C:\>Find-AzureRmResourceGroup -Tag @{ "testtag" = $null }
```

<span data-ttu-id="38396-111">To polecenie umożliwia znalezienie wszystkich grup zasobów mających znacznik o nazwie testtag.</span><span class="sxs-lookup"><span data-stu-id="38396-111">This command finds all resource groups that have a tag named testtag.</span></span>

### <span data-ttu-id="38396-112">Przykład 3: Znajdowanie grup zasobów według nazwy i wartości znacznika</span><span class="sxs-lookup"><span data-stu-id="38396-112">Example 3: Find resource groups by tag name and value</span></span>
```
PS C:\>Find-AzureRmResourceGroup -Tag @{"testtag" = "testval" }
```

<span data-ttu-id="38396-113">To polecenie umożliwia znalezienie wszystkich grup zasobów mających znacznik o nazwie testtag oraz wartość testval.</span><span class="sxs-lookup"><span data-stu-id="38396-113">This command finds all resource groups that have a tag named testtag and the value testval.</span></span>

## <span data-ttu-id="38396-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="38396-114">PARAMETERS</span></span>

### <span data-ttu-id="38396-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="38396-115">-ApiVersion</span></span>
<span data-ttu-id="38396-116">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="38396-116">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="38396-117">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="38396-117">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38396-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38396-118">-DefaultProfile</span></span>
<span data-ttu-id="38396-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="38396-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="38396-120">-Pre</span><span class="sxs-lookup"><span data-stu-id="38396-120">-Pre</span></span>
<span data-ttu-id="38396-121">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="38396-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38396-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="38396-122">-Tag</span></span>
<span data-ttu-id="38396-123">Określa informacje znacznika jako tabelę skrótów, aby filtrować wyniki.</span><span class="sxs-lookup"><span data-stu-id="38396-123">Specifies tag information, as a hash table, to filter your results.</span></span> <span data-ttu-id="38396-124">Użyj następujących formatów:</span><span class="sxs-lookup"><span data-stu-id="38396-124">Use the following formats:</span></span>

<span data-ttu-id="38396-125">@ {tagName = $null} lub @ {tagName = ' tagValue '}.</span><span class="sxs-lookup"><span data-stu-id="38396-125">@{tagName=$null} or @{tagName = 'tagValue'}.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38396-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38396-126">CommonParameters</span></span>
<span data-ttu-id="38396-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38396-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38396-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38396-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38396-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="38396-129">INPUTS</span></span>

### <span data-ttu-id="38396-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="38396-130">None</span></span>
<span data-ttu-id="38396-131">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="38396-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="38396-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="38396-132">OUTPUTS</span></span>

### <span data-ttu-id="38396-133">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="38396-133">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="38396-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="38396-134">NOTES</span></span>

## <span data-ttu-id="38396-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="38396-135">RELATED LINKS</span></span>
