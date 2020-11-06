---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppSlotPublishingProfile.md
ms.openlocfilehash: b6a01079bed80017054e7fe52673012827dce02d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525457"
---
# <span data-ttu-id="851d2-101">Reset-AzureRmWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="851d2-101">Reset-AzureRmWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="851d2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="851d2-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="851d2-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="851d2-103">SYNTAX</span></span>

### <span data-ttu-id="851d2-104">S1</span><span class="sxs-lookup"><span data-stu-id="851d2-104">S1</span></span>
```
Reset-AzureRmWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="851d2-105">S2</span><span class="sxs-lookup"><span data-stu-id="851d2-105">S2</span></span>
```
Reset-AzureRmWebAppSlotPublishingProfile [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="851d2-106">Opis</span><span class="sxs-lookup"><span data-stu-id="851d2-106">DESCRIPTION</span></span>
<span data-ttu-id="851d2-107">Polecenie cmdlet **Reset-AzureRmWebAppSlotPublishingProfile** resetuje profil publikowania dla określonego miejsca aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="851d2-107">The **Reset-AzureRmWebAppSlotPublishingProfile** cmdlet resets the publishing profile for the specified Web App Slot.</span></span>

## <span data-ttu-id="851d2-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="851d2-108">EXAMPLES</span></span>

### <span data-ttu-id="851d2-109">1:1</span><span class="sxs-lookup"><span data-stu-id="851d2-109">1:</span></span>
```
PS C:\> Reset-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

<span data-ttu-id="851d2-110">To polecenie resetuje profil publikowania dla gniazda o nazwie slot001 dla aplikacji sieci Web ContosoWebApp skojarzonego z domyślną grupą zasobów — Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="851d2-110">This command resets the publishing profile for the Slot named slot001 for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="851d2-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="851d2-111">PARAMETERS</span></span>

### <span data-ttu-id="851d2-112">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="851d2-112">-Name</span></span>
<span data-ttu-id="851d2-113">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="851d2-113">WebApp Name</span></span>

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

### <span data-ttu-id="851d2-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="851d2-114">-ResourceGroupName</span></span>
<span data-ttu-id="851d2-115">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="851d2-115">Resource Group Name</span></span>

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

### <span data-ttu-id="851d2-116">-Slot</span><span class="sxs-lookup"><span data-stu-id="851d2-116">-Slot</span></span>
<span data-ttu-id="851d2-117">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="851d2-117">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="851d2-118">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="851d2-118">-WebApp</span></span>
<span data-ttu-id="851d2-119">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="851d2-119">WebApp Object</span></span>

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

### <span data-ttu-id="851d2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="851d2-120">-DefaultProfile</span></span>
<span data-ttu-id="851d2-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="851d2-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="851d2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="851d2-122">CommonParameters</span></span>
<span data-ttu-id="851d2-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="851d2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="851d2-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="851d2-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="851d2-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="851d2-125">INPUTS</span></span>

### <span data-ttu-id="851d2-126">Klienta</span><span class="sxs-lookup"><span data-stu-id="851d2-126">Site</span></span>
<span data-ttu-id="851d2-127">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="851d2-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="851d2-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="851d2-128">OUTPUTS</span></span>

## <span data-ttu-id="851d2-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="851d2-129">NOTES</span></span>

## <span data-ttu-id="851d2-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="851d2-130">RELATED LINKS</span></span>

