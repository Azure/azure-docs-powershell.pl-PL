---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotConfigName.md
ms.openlocfilehash: b1b9760d129a4177f979996f1ef46bd2a225f452
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93710916"
---
# <span data-ttu-id="6942c-101">Get-AzureRmWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="6942c-101">Get-AzureRmWebAppSlotConfigName</span></span>

## <span data-ttu-id="6942c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6942c-102">SYNOPSIS</span></span>
<span data-ttu-id="6942c-103">Uzyskiwanie listy nazw konfiguracji miejsca aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="6942c-103">Get the list of Web App Slot Config names</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6942c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6942c-104">SYNTAX</span></span>

### <span data-ttu-id="6942c-105">S1</span><span class="sxs-lookup"><span data-stu-id="6942c-105">S1</span></span>
```
Get-AzureRmWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6942c-106">S2</span><span class="sxs-lookup"><span data-stu-id="6942c-106">S2</span></span>
```
Get-AzureRmWebAppSlotConfigName [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6942c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="6942c-107">DESCRIPTION</span></span>
<span data-ttu-id="6942c-108">Polecenie cmdlet **Get-AzureRmWebAppSlotConfigName** pobiera listę nazw ustawień aplikacji i parametrów połączeń, które są obecnie oznaczone jako ustawienia gniazd</span><span class="sxs-lookup"><span data-stu-id="6942c-108">The **Get-AzureRmWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="6942c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6942c-109">EXAMPLES</span></span>

### <span data-ttu-id="6942c-110">1:1</span><span class="sxs-lookup"><span data-stu-id="6942c-110">1:</span></span>
```
PS C:\>Get-AzureRmWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="6942c-111">To polecenie pobiera ustawienia aplikacji i ciągi połączeń odnoszące się do aplikacji sieci Web o nazwie ContosoSite skojarzonej z domyślnym grupą zasobów — sieć Web-zachód.</span><span class="sxs-lookup"><span data-stu-id="6942c-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="6942c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6942c-112">PARAMETERS</span></span>

### <span data-ttu-id="6942c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6942c-113">-DefaultProfile</span></span>
<span data-ttu-id="6942c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6942c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6942c-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6942c-115">-Name</span></span>
<span data-ttu-id="6942c-116">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="6942c-116">WebApp Name</span></span>

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

### <span data-ttu-id="6942c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6942c-117">-ResourceGroupName</span></span>
<span data-ttu-id="6942c-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="6942c-118">Resource Group Name</span></span>

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

### <span data-ttu-id="6942c-119">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="6942c-119">-WebApp</span></span>
<span data-ttu-id="6942c-120">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="6942c-120">WebApp Object</span></span>

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

### <span data-ttu-id="6942c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6942c-121">CommonParameters</span></span>
<span data-ttu-id="6942c-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6942c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6942c-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6942c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6942c-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6942c-124">INPUTS</span></span>

### <span data-ttu-id="6942c-125">System. String</span><span class="sxs-lookup"><span data-stu-id="6942c-125">System.String</span></span>

### <span data-ttu-id="6942c-126">Microsoft. Azure. Management. Web. models. site</span><span class="sxs-lookup"><span data-stu-id="6942c-126">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="6942c-127">Parametry: aplikacji (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6942c-127">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="6942c-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6942c-128">OUTPUTS</span></span>

### <span data-ttu-id="6942c-129">Microsoft. Azure. Management. Web. MODELES. SlotConfigNamesResource</span><span class="sxs-lookup"><span data-stu-id="6942c-129">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span></span>

## <span data-ttu-id="6942c-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6942c-130">NOTES</span></span>

## <span data-ttu-id="6942c-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6942c-131">RELATED LINKS</span></span>
