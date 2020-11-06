---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppPublishingProfile.md
ms.openlocfilehash: f1224ae7ad95598d8ae947d0e38ef3a9cf7a4dba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528182"
---
# <span data-ttu-id="76cf5-101">Reset-AzureRmWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="76cf5-101">Reset-AzureRmWebAppPublishingProfile</span></span>

## <span data-ttu-id="76cf5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="76cf5-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76cf5-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="76cf5-103">SYNTAX</span></span>

### <span data-ttu-id="76cf5-104">S1</span><span class="sxs-lookup"><span data-stu-id="76cf5-104">S1</span></span>
```
Reset-AzureRmWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76cf5-105">S2</span><span class="sxs-lookup"><span data-stu-id="76cf5-105">S2</span></span>
```
Reset-AzureRmWebAppPublishingProfile [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="76cf5-106">Opis</span><span class="sxs-lookup"><span data-stu-id="76cf5-106">DESCRIPTION</span></span>
<span data-ttu-id="76cf5-107">Polecenie cmdlet **Reset-AzureRmWebAppPublishingProfile** resetuje profil publikowania dla określonej aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="76cf5-107">The **Reset-AzureRmWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="76cf5-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="76cf5-108">EXAMPLES</span></span>

### <span data-ttu-id="76cf5-109">1:1</span><span class="sxs-lookup"><span data-stu-id="76cf5-109">1:</span></span>
```
PS C:\> Reset-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="76cf5-110">To polecenie resetuje profil publikowania dla aplikacji sieci Web ContosoWebApp skojarzonego z domyślnym grupą zasobów — sieć Web — zachód.</span><span class="sxs-lookup"><span data-stu-id="76cf5-110">This command resets the publishing profile for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="76cf5-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="76cf5-111">PARAMETERS</span></span>

### <span data-ttu-id="76cf5-112">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="76cf5-112">-Name</span></span>
<span data-ttu-id="76cf5-113">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="76cf5-113">WebApp Name</span></span>

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

### <span data-ttu-id="76cf5-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76cf5-114">-ResourceGroupName</span></span>
<span data-ttu-id="76cf5-115">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="76cf5-115">Resource Group Name</span></span>

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

### <span data-ttu-id="76cf5-116">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="76cf5-116">-WebApp</span></span>
<span data-ttu-id="76cf5-117">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="76cf5-117">WebApp Object</span></span>

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

### <span data-ttu-id="76cf5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76cf5-118">-DefaultProfile</span></span>
<span data-ttu-id="76cf5-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="76cf5-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76cf5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76cf5-120">CommonParameters</span></span>
<span data-ttu-id="76cf5-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76cf5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76cf5-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76cf5-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76cf5-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="76cf5-123">INPUTS</span></span>

### <span data-ttu-id="76cf5-124">Klienta</span><span class="sxs-lookup"><span data-stu-id="76cf5-124">Site</span></span>
<span data-ttu-id="76cf5-125">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="76cf5-125">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="76cf5-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="76cf5-126">OUTPUTS</span></span>

## <span data-ttu-id="76cf5-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="76cf5-127">NOTES</span></span>

## <span data-ttu-id="76cf5-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="76cf5-128">RELATED LINKS</span></span>

