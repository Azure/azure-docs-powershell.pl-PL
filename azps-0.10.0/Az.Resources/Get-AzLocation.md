---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DC870E11-2129-4906-8357-D9BC1CF2E08E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzLocation.md
ms.openlocfilehash: 4aedbb502780a08d0ce5556af84a445ab44552f5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892609"
---
# <span data-ttu-id="54948-101">Get-AzLocation</span><span class="sxs-lookup"><span data-stu-id="54948-101">Get-AzLocation</span></span>

## <span data-ttu-id="54948-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="54948-102">SYNOPSIS</span></span>
<span data-ttu-id="54948-103">Pobiera wszystkie lokalizacje i dostawców zasobów obsługiwanych dla każdej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="54948-103">Gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="54948-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="54948-104">SYNTAX</span></span>

```
Get-AzLocation [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="54948-105">Opis</span><span class="sxs-lookup"><span data-stu-id="54948-105">DESCRIPTION</span></span>
<span data-ttu-id="54948-106">Polecenie cmdlet **Get-AzLocation** pobiera wszystkie lokalizacje i dostawców zasobów obsługiwanych dla każdej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="54948-106">The **Get-AzLocation** cmdlet gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="54948-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="54948-107">EXAMPLES</span></span>

### <span data-ttu-id="54948-108">Przykład 1: pobieranie wszystkich lokalizacji i obsługiwanych dostawców zasobów</span><span class="sxs-lookup"><span data-stu-id="54948-108">Example 1: Get all locations and the supported resource providers</span></span>
```
PS C:\>Get-AzLocation
```

<span data-ttu-id="54948-109">To polecenie pobiera wszystkie lokalizacje i dostawców zasobów obsługiwanych dla każdej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="54948-109">This command gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="54948-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="54948-110">PARAMETERS</span></span>

### <span data-ttu-id="54948-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="54948-111">-ApiVersion</span></span>
<span data-ttu-id="54948-112">Określa wersję API obsługiwaną przez dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="54948-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="54948-113">Możesz określić inną wersję niż wersja domyślna.</span><span class="sxs-lookup"><span data-stu-id="54948-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="54948-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54948-114">-DefaultProfile</span></span>
<span data-ttu-id="54948-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="54948-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54948-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="54948-116">-Pre</span></span>
<span data-ttu-id="54948-117">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="54948-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54948-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54948-118">CommonParameters</span></span>
<span data-ttu-id="54948-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54948-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54948-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54948-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54948-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="54948-121">INPUTS</span></span>

## <span data-ttu-id="54948-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="54948-122">OUTPUTS</span></span>

## <span data-ttu-id="54948-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="54948-123">NOTES</span></span>

## <span data-ttu-id="54948-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="54948-124">RELATED LINKS</span></span>
