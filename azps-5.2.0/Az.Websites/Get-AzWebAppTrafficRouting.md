---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppTrafficRouting.md
ms.openlocfilehash: fb8d23ad24f8e9ab0b6e951d39ba7445d336176f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367115"
---
# <span data-ttu-id="76a81-101">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="76a81-101">Get-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="76a81-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="76a81-102">SYNOPSIS</span></span>
<span data-ttu-id="76a81-103">Pobierz regułę routingu dla danej nazwy miejsca.</span><span class="sxs-lookup"><span data-stu-id="76a81-103">Get a routing Rule for the given Slot name.</span></span>

## <span data-ttu-id="76a81-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="76a81-104">SYNTAX</span></span>

```
Get-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RuleName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76a81-105">Opis</span><span class="sxs-lookup"><span data-stu-id="76a81-105">DESCRIPTION</span></span>
<span data-ttu-id="76a81-106">Polecenie cmdlet **Get-AzWebAppTrafficRouting** Pobiera konfigurację reguły routingu z miejsca w aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="76a81-106">The **Get-AzWebAppTrafficRouting** cmdlet Gets a routing rule configuration from an Azure Web App Slot.</span></span>

## <span data-ttu-id="76a81-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="76a81-107">EXAMPLES</span></span>

### <span data-ttu-id="76a81-108">Przykład 1 pobiera określoną regułę routingu z gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="76a81-108">Example 1 Gets the specific routing rule from webapp slot</span></span>
```powershell
PS C:\> Get-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite"  -RuleName 'Stg'
```

<span data-ttu-id="76a81-109">To polecenie pobiera regułę routingu dla danego gniazda aplikacji.</span><span class="sxs-lookup"><span data-stu-id="76a81-109">This command gets a routing rule for a given webapp slot.</span></span>

## <span data-ttu-id="76a81-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="76a81-110">PARAMETERS</span></span>

### <span data-ttu-id="76a81-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76a81-111">-DefaultProfile</span></span>
<span data-ttu-id="76a81-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="76a81-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76a81-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76a81-113">-ResourceGroupName</span></span>
<span data-ttu-id="76a81-114">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="76a81-114">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76a81-115">-RuleName</span><span class="sxs-lookup"><span data-stu-id="76a81-115">-RuleName</span></span>
<span data-ttu-id="76a81-116">Nazwa reguły</span><span class="sxs-lookup"><span data-stu-id="76a81-116">Rule Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76a81-117">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="76a81-117">-WebAppName</span></span>
<span data-ttu-id="76a81-118">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="76a81-118">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76a81-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76a81-119">CommonParameters</span></span>
<span data-ttu-id="76a81-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76a81-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76a81-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76a81-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76a81-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="76a81-122">INPUTS</span></span>

### <span data-ttu-id="76a81-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="76a81-123">None</span></span>

## <span data-ttu-id="76a81-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="76a81-124">OUTPUTS</span></span>

### <span data-ttu-id="76a81-125">Microsoft. Azure. Management. Web. MODELES. RampUpRule</span><span class="sxs-lookup"><span data-stu-id="76a81-125">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="76a81-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="76a81-126">NOTES</span></span>

## <span data-ttu-id="76a81-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="76a81-127">RELATED LINKS</span></span>

[<span data-ttu-id="76a81-128">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="76a81-128">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)

[<span data-ttu-id="76a81-129">Dodaj-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="76a81-129">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="76a81-130">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="76a81-130">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)
