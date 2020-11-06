---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotConfigName.md
ms.openlocfilehash: 96e9c5945938addfbd629ef66b5f68e54c0427e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542120"
---
# <span data-ttu-id="56df8-101">Get-AzureRmWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="56df8-101">Get-AzureRmWebAppSlotConfigName</span></span>

## <span data-ttu-id="56df8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="56df8-102">SYNOPSIS</span></span>
<span data-ttu-id="56df8-103">Uzyskiwanie listy nazw konfiguracji miejsca aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="56df8-103">Get the list of Web App Slot Config names</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56df8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="56df8-104">SYNTAX</span></span>

### <span data-ttu-id="56df8-105">S1</span><span class="sxs-lookup"><span data-stu-id="56df8-105">S1</span></span>
```
Get-AzureRmWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56df8-106">S2</span><span class="sxs-lookup"><span data-stu-id="56df8-106">S2</span></span>
```
Get-AzureRmWebAppSlotConfigName [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="56df8-107">Opis</span><span class="sxs-lookup"><span data-stu-id="56df8-107">DESCRIPTION</span></span>
<span data-ttu-id="56df8-108">Polecenie cmdlet **Get-AzureRmWebAppSlotConfigName** pobiera listę nazw ustawień aplikacji i parametrów połączeń, które są obecnie oznaczone jako ustawienia gniazd</span><span class="sxs-lookup"><span data-stu-id="56df8-108">The **Get-AzureRmWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="56df8-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="56df8-109">EXAMPLES</span></span>

### <span data-ttu-id="56df8-110">1:1</span><span class="sxs-lookup"><span data-stu-id="56df8-110">1:</span></span>
```
PS C:\>Get-AzureRmWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="56df8-111">To polecenie pobiera ustawienia aplikacji i ciągi połączeń odnoszące się do aplikacji sieci Web o nazwie ContosoSite skojarzonej z domyślnym grupą zasobów — sieć Web-zachód.</span><span class="sxs-lookup"><span data-stu-id="56df8-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="56df8-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="56df8-112">PARAMETERS</span></span>

### <span data-ttu-id="56df8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56df8-113">-DefaultProfile</span></span>
<span data-ttu-id="56df8-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="56df8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56df8-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="56df8-115">-Name</span></span>
<span data-ttu-id="56df8-116">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="56df8-116">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56df8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56df8-117">-ResourceGroupName</span></span>
<span data-ttu-id="56df8-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="56df8-118">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56df8-119">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="56df8-119">-WebApp</span></span>
<span data-ttu-id="56df8-120">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="56df8-120">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56df8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56df8-121">CommonParameters</span></span>
<span data-ttu-id="56df8-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56df8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56df8-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56df8-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56df8-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="56df8-124">INPUTS</span></span>

### <span data-ttu-id="56df8-125">Klienta</span><span class="sxs-lookup"><span data-stu-id="56df8-125">Site</span></span>
<span data-ttu-id="56df8-126">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="56df8-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="56df8-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="56df8-127">OUTPUTS</span></span>

## <span data-ttu-id="56df8-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="56df8-128">NOTES</span></span>

## <span data-ttu-id="56df8-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="56df8-129">RELATED LINKS</span></span>

