---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: https://docs.microsoft.com/powershell/module/az.websites/reset-azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: bdee1c1fdda561d7265b3f6ff52a443238b6d2b7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995814"
---
# <span data-ttu-id="a3f2a-101">Reset-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="a3f2a-101">Reset-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="a3f2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3f2a-102">SYNOPSIS</span></span>

## <span data-ttu-id="a3f2a-103">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a3f2a-103">SYNTAX</span></span>

### <span data-ttu-id="a3f2a-104">S1</span><span class="sxs-lookup"><span data-stu-id="a3f2a-104">S1</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3f2a-105">S2</span><span class="sxs-lookup"><span data-stu-id="a3f2a-105">S2</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a3f2a-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="a3f2a-106">DESCRIPTION</span></span>
<span data-ttu-id="a3f2a-107">Polecenie **cmdlet Reset-AzWebAppSlotPublishingProfile** resetuje profil publikowania dla określonego miejsca aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="a3f2a-107">The **Reset-AzWebAppSlotPublishingProfile** cmdlet resets the publishing profile for the specified Web App Slot.</span></span>

## <span data-ttu-id="a3f2a-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a3f2a-108">EXAMPLES</span></span>

### <span data-ttu-id="a3f2a-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a3f2a-109">Example 1</span></span>
```powershell
PS C:\> Reset-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

<span data-ttu-id="a3f2a-110">To polecenie powoduje zresetowanie profilu publikowania dla typu Slot o nazwie slot001 dla aplikacji Web App ContosoWebApp skojarzonej z grupą zasobów Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="a3f2a-110">This command resets the publishing profile for the Slot named slot001 for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="a3f2a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3f2a-111">PARAMETERS</span></span>

### <span data-ttu-id="a3f2a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3f2a-112">-DefaultProfile</span></span>
<span data-ttu-id="a3f2a-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a3f2a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3f2a-114">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a3f2a-114">-Name</span></span>
<span data-ttu-id="a3f2a-115">Nazwa aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="a3f2a-115">WebApp Name</span></span>

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

### <span data-ttu-id="a3f2a-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3f2a-116">-ResourceGroupName</span></span>
<span data-ttu-id="a3f2a-117">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a3f2a-117">Resource Group Name</span></span>

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

### <span data-ttu-id="a3f2a-118">— Slot</span><span class="sxs-lookup"><span data-stu-id="a3f2a-118">-Slot</span></span>
<span data-ttu-id="a3f2a-119">Nazwa gniazda aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="a3f2a-119">WebApp Slot Name</span></span>

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

### <span data-ttu-id="a3f2a-120">- WebApp</span><span class="sxs-lookup"><span data-stu-id="a3f2a-120">-WebApp</span></span>
<span data-ttu-id="a3f2a-121">Obiekt WebApp</span><span class="sxs-lookup"><span data-stu-id="a3f2a-121">WebApp Object</span></span>

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

### <span data-ttu-id="a3f2a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3f2a-122">CommonParameters</span></span>
<span data-ttu-id="a3f2a-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3f2a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3f2a-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3f2a-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3f2a-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a3f2a-125">INPUTS</span></span>

### <span data-ttu-id="a3f2a-126">System.String</span><span class="sxs-lookup"><span data-stu-id="a3f2a-126">System.String</span></span>

### <span data-ttu-id="a3f2a-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="a3f2a-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="a3f2a-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a3f2a-128">OUTPUTS</span></span>

### <span data-ttu-id="a3f2a-129">System.String</span><span class="sxs-lookup"><span data-stu-id="a3f2a-129">System.String</span></span>

## <span data-ttu-id="a3f2a-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a3f2a-130">NOTES</span></span>

## <span data-ttu-id="a3f2a-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a3f2a-131">RELATED LINKS</span></span>
