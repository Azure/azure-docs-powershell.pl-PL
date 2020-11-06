---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/reset-azurermwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppPublishingProfile.md
ms.openlocfilehash: b519012104472d9b97f5f0a5e4b699829b99fff4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551460"
---
# <span data-ttu-id="1bb81-101">Reset-AzureRmWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="1bb81-101">Reset-AzureRmWebAppPublishingProfile</span></span>

## <span data-ttu-id="1bb81-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1bb81-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1bb81-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1bb81-103">SYNTAX</span></span>

### <span data-ttu-id="1bb81-104">S1</span><span class="sxs-lookup"><span data-stu-id="1bb81-104">S1</span></span>
```
Reset-AzureRmWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1bb81-105">S2</span><span class="sxs-lookup"><span data-stu-id="1bb81-105">S2</span></span>
```
Reset-AzureRmWebAppPublishingProfile [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1bb81-106">Opis</span><span class="sxs-lookup"><span data-stu-id="1bb81-106">DESCRIPTION</span></span>
<span data-ttu-id="1bb81-107">Polecenie cmdlet **Reset-AzureRmWebAppPublishingProfile** resetuje profil publikowania dla określonej aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="1bb81-107">The **Reset-AzureRmWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="1bb81-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1bb81-108">EXAMPLES</span></span>

### <span data-ttu-id="1bb81-109">1:1</span><span class="sxs-lookup"><span data-stu-id="1bb81-109">1:</span></span>
```
PS C:\> Reset-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="1bb81-110">To polecenie resetuje profil publikowania dla aplikacji sieci Web ContosoWebApp skojarzonego z domyślnym grupą zasobów — sieć Web — zachód.</span><span class="sxs-lookup"><span data-stu-id="1bb81-110">This command resets the publishing profile for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="1bb81-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1bb81-111">PARAMETERS</span></span>

### <span data-ttu-id="1bb81-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bb81-112">-DefaultProfile</span></span>
<span data-ttu-id="1bb81-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1bb81-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1bb81-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1bb81-114">-Name</span></span>
<span data-ttu-id="1bb81-115">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="1bb81-115">WebApp Name</span></span>

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

### <span data-ttu-id="1bb81-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bb81-116">-ResourceGroupName</span></span>
<span data-ttu-id="1bb81-117">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="1bb81-117">Resource Group Name</span></span>

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

### <span data-ttu-id="1bb81-118">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="1bb81-118">-WebApp</span></span>
<span data-ttu-id="1bb81-119">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="1bb81-119">WebApp Object</span></span>

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

### <span data-ttu-id="1bb81-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bb81-120">CommonParameters</span></span>
<span data-ttu-id="1bb81-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bb81-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bb81-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bb81-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bb81-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1bb81-123">INPUTS</span></span>

### <span data-ttu-id="1bb81-124">Klienta</span><span class="sxs-lookup"><span data-stu-id="1bb81-124">Site</span></span>
<span data-ttu-id="1bb81-125">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="1bb81-125">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="1bb81-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1bb81-126">OUTPUTS</span></span>

## <span data-ttu-id="1bb81-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1bb81-127">NOTES</span></span>

## <span data-ttu-id="1bb81-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1bb81-128">RELATED LINKS</span></span>

