---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/reset-azurermwebapppublishingprofile
schema: 2.0.0
ms.openlocfilehash: f082241be9e31b11782fcbbf5570a7f3c3947012
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897205"
---
# <span data-ttu-id="b4724-101">Reset-AzureRmWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="b4724-101">Reset-AzureRmWebAppPublishingProfile</span></span>

## <span data-ttu-id="b4724-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b4724-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4724-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b4724-103">SYNTAX</span></span>

### <span data-ttu-id="b4724-104">S1</span><span class="sxs-lookup"><span data-stu-id="b4724-104">S1</span></span>
```
Reset-AzureRmWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4724-105">S2</span><span class="sxs-lookup"><span data-stu-id="b4724-105">S2</span></span>
```
Reset-AzureRmWebAppPublishingProfile [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b4724-106">Opis</span><span class="sxs-lookup"><span data-stu-id="b4724-106">DESCRIPTION</span></span>
<span data-ttu-id="b4724-107">Polecenie cmdlet **Reset-AzureRmWebAppPublishingProfile** resetuje profil publikowania dla określonej aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="b4724-107">The **Reset-AzureRmWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="b4724-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b4724-108">EXAMPLES</span></span>

### <span data-ttu-id="b4724-109">1:1</span><span class="sxs-lookup"><span data-stu-id="b4724-109">1:</span></span>
```
PS C:\> Reset-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="b4724-110">To polecenie resetuje profil publikowania dla aplikacji sieci Web ContosoWebApp skojarzonego z domyślnym grupą zasobów — sieć Web — zachód.</span><span class="sxs-lookup"><span data-stu-id="b4724-110">This command resets the publishing profile for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="b4724-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b4724-111">PARAMETERS</span></span>

### <span data-ttu-id="b4724-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4724-112">-DefaultProfile</span></span>
<span data-ttu-id="b4724-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b4724-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4724-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b4724-114">-Name</span></span>
<span data-ttu-id="b4724-115">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="b4724-115">WebApp Name</span></span>

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

### <span data-ttu-id="b4724-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4724-116">-ResourceGroupName</span></span>
<span data-ttu-id="b4724-117">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b4724-117">Resource Group Name</span></span>

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

### <span data-ttu-id="b4724-118">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="b4724-118">-WebApp</span></span>
<span data-ttu-id="b4724-119">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="b4724-119">WebApp Object</span></span>

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

### <span data-ttu-id="b4724-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4724-120">CommonParameters</span></span>
<span data-ttu-id="b4724-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4724-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4724-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4724-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4724-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b4724-123">INPUTS</span></span>

### <span data-ttu-id="b4724-124">Klienta</span><span class="sxs-lookup"><span data-stu-id="b4724-124">Site</span></span>
<span data-ttu-id="b4724-125">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="b4724-125">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="b4724-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b4724-126">OUTPUTS</span></span>

## <span data-ttu-id="b4724-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b4724-127">NOTES</span></span>

## <span data-ttu-id="b4724-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b4724-128">RELATED LINKS</span></span>

