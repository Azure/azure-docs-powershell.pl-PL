---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
ms.openlocfilehash: 9ca0578aacbd0ca970211bc38419880cbe99675b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98498086"
---
# <span data-ttu-id="4b71e-101">Get-AzWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="4b71e-101">Get-AzWebAppSlotConfigName</span></span>

## <span data-ttu-id="4b71e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4b71e-102">SYNOPSIS</span></span>
<span data-ttu-id="4b71e-103">Uzyskiwanie listy nazw konfiguracji miejsca aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="4b71e-103">Get the list of Web App Slot Config names</span></span>

## <span data-ttu-id="4b71e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4b71e-104">SYNTAX</span></span>

### <span data-ttu-id="4b71e-105">S1</span><span class="sxs-lookup"><span data-stu-id="4b71e-105">S1</span></span>
```
Get-AzWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b71e-106">S2</span><span class="sxs-lookup"><span data-stu-id="4b71e-106">S2</span></span>
```
Get-AzWebAppSlotConfigName [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b71e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4b71e-107">DESCRIPTION</span></span>
<span data-ttu-id="4b71e-108">Polecenie cmdlet **Get-AzWebAppSlotConfigName** pobiera listę nazw ustawień aplikacji i parametrów połączeń, które są obecnie oznaczone jako ustawienia gniazd</span><span class="sxs-lookup"><span data-stu-id="4b71e-108">The **Get-AzWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="4b71e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4b71e-109">EXAMPLES</span></span>

### <span data-ttu-id="4b71e-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4b71e-110">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="4b71e-111">To polecenie pobiera ustawienia aplikacji i ciągi połączeń odnoszące się do aplikacji sieci Web o nazwie ContosoSite skojarzonej z domyślnym grupą zasobów — sieć Web-zachód.</span><span class="sxs-lookup"><span data-stu-id="4b71e-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="4b71e-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4b71e-112">PARAMETERS</span></span>

### <span data-ttu-id="4b71e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b71e-113">-DefaultProfile</span></span>
<span data-ttu-id="4b71e-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4b71e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b71e-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4b71e-115">-Name</span></span>
<span data-ttu-id="4b71e-116">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="4b71e-116">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b71e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b71e-117">-ResourceGroupName</span></span>
<span data-ttu-id="4b71e-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="4b71e-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b71e-119">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="4b71e-119">-WebApp</span></span>
<span data-ttu-id="4b71e-120">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="4b71e-120">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4b71e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b71e-121">CommonParameters</span></span>
<span data-ttu-id="4b71e-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b71e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b71e-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b71e-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b71e-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4b71e-124">INPUTS</span></span>

### <span data-ttu-id="4b71e-125">System. String</span><span class="sxs-lookup"><span data-stu-id="4b71e-125">System.String</span></span>

### <span data-ttu-id="4b71e-126">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="4b71e-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="4b71e-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4b71e-127">OUTPUTS</span></span>

### <span data-ttu-id="4b71e-128">Microsoft. Azure. Management. Web. MODELES. SlotConfigNamesResource</span><span class="sxs-lookup"><span data-stu-id="4b71e-128">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span></span>

## <span data-ttu-id="4b71e-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4b71e-129">NOTES</span></span>

## <span data-ttu-id="4b71e-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4b71e-130">RELATED LINKS</span></span>
