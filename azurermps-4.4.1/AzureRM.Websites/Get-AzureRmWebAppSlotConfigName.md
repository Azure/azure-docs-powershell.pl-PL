---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotConfigName.md
ms.openlocfilehash: 196e653447204b65c7f431e29fe76078a268dda1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718973"
---
# <span data-ttu-id="b1087-101">Get-AzureRmWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="b1087-101">Get-AzureRmWebAppSlotConfigName</span></span>

## <span data-ttu-id="b1087-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b1087-102">SYNOPSIS</span></span>
<span data-ttu-id="b1087-103">Uzyskiwanie listy nazw konfiguracji miejsca aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="b1087-103">Get the list of Web App Slot Config names</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1087-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b1087-104">SYNTAX</span></span>

### <span data-ttu-id="b1087-105">S1</span><span class="sxs-lookup"><span data-stu-id="b1087-105">S1</span></span>
```
Get-AzureRmWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1087-106">S2</span><span class="sxs-lookup"><span data-stu-id="b1087-106">S2</span></span>
```
Get-AzureRmWebAppSlotConfigName [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b1087-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b1087-107">DESCRIPTION</span></span>
<span data-ttu-id="b1087-108">Polecenie cmdlet **Get-AzureRmWebAppSlotConfigName** pobiera listę nazw ustawień aplikacji i parametrów połączeń, które są obecnie oznaczone jako ustawienia gniazd</span><span class="sxs-lookup"><span data-stu-id="b1087-108">The **Get-AzureRmWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="b1087-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b1087-109">EXAMPLES</span></span>

### <span data-ttu-id="b1087-110">1:1</span><span class="sxs-lookup"><span data-stu-id="b1087-110">1:</span></span>
```
PS C:\>Get-AzureRmWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="b1087-111">To polecenie pobiera ustawienia aplikacji i ciągi połączeń odnoszące się do aplikacji sieci Web o nazwie ContosoSite skojarzonej z domyślnym grupą zasobów — sieć Web-zachód.</span><span class="sxs-lookup"><span data-stu-id="b1087-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="b1087-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b1087-112">PARAMETERS</span></span>

### <span data-ttu-id="b1087-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b1087-113">-Name</span></span>
<span data-ttu-id="b1087-114">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="b1087-114">WebApp Name</span></span>

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

### <span data-ttu-id="b1087-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1087-115">-ResourceGroupName</span></span>
<span data-ttu-id="b1087-116">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b1087-116">Resource Group Name</span></span>

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

### <span data-ttu-id="b1087-117">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="b1087-117">-WebApp</span></span>
<span data-ttu-id="b1087-118">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="b1087-118">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1087-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1087-119">-DefaultProfile</span></span>
<span data-ttu-id="b1087-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b1087-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1087-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1087-121">CommonParameters</span></span>
<span data-ttu-id="b1087-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1087-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1087-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1087-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1087-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b1087-124">INPUTS</span></span>

### <span data-ttu-id="b1087-125">Klienta</span><span class="sxs-lookup"><span data-stu-id="b1087-125">Site</span></span>
<span data-ttu-id="b1087-126">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="b1087-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="b1087-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b1087-127">OUTPUTS</span></span>

## <span data-ttu-id="b1087-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b1087-128">NOTES</span></span>

## <span data-ttu-id="b1087-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b1087-129">RELATED LINKS</span></span>

