---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 86E0D477-DD32-49BD-82E7-1CF191E4F612
online version: https://docs.microsoft.com/powershell/module/az.websites/stop-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebAppSlot.md
ms.openlocfilehash: 1be0602fc139c5630591dea1e7aa35eaaf27a714
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011002"
---
# <span data-ttu-id="de822-101">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="de822-101">Stop-AzWebAppSlot</span></span>

## <span data-ttu-id="de822-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de822-102">SYNOPSIS</span></span>
<span data-ttu-id="de822-103">Zatrzymuje miejsce na aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="de822-103">Stops an Azure Web App slot.</span></span>

## <span data-ttu-id="de822-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="de822-104">SYNTAX</span></span>

### <span data-ttu-id="de822-105">S1</span><span class="sxs-lookup"><span data-stu-id="de822-105">S1</span></span>
```
Stop-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de822-106">S2</span><span class="sxs-lookup"><span data-stu-id="de822-106">S2</span></span>
```
Stop-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de822-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="de822-107">DESCRIPTION</span></span>
<span data-ttu-id="de822-108">Polecenie **cmdlet Stop-AzWebAppSlot** zatrzymuje miejsce aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="de822-108">The **Stop-AzWebAppSlot** cmdlet stops an Azure Web App Slot.</span></span>

## <span data-ttu-id="de822-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="de822-109">EXAMPLES</span></span>

### <span data-ttu-id="de822-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="de822-110">Example 1</span></span>
```
PS C:\>Stop-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="de822-111">To polecenie zatrzymuje miejsce Slot001 odnoszące się do aplikacji sieci Web o nazwie ContosoWebApp, które należy do grupy zasobów o nazwie Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="de822-111">This command stops the slot Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="de822-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="de822-112">PARAMETERS</span></span>

### <span data-ttu-id="de822-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de822-113">-DefaultProfile</span></span>
<span data-ttu-id="de822-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="de822-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de822-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="de822-115">-Name</span></span>
<span data-ttu-id="de822-116">Nazwa aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="de822-116">WebApp Name</span></span>

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

### <span data-ttu-id="de822-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de822-117">-ResourceGroupName</span></span>
<span data-ttu-id="de822-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="de822-118">Resource Group Name</span></span>

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

### <span data-ttu-id="de822-119">— Slot</span><span class="sxs-lookup"><span data-stu-id="de822-119">-Slot</span></span>
<span data-ttu-id="de822-120">Nazwa gniazda aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="de822-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="de822-121">- WebApp</span><span class="sxs-lookup"><span data-stu-id="de822-121">-WebApp</span></span>
<span data-ttu-id="de822-122">Obiekt WebApp</span><span class="sxs-lookup"><span data-stu-id="de822-122">WebApp Object</span></span>

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

### <span data-ttu-id="de822-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de822-123">CommonParameters</span></span>
<span data-ttu-id="de822-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de822-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de822-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de822-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de822-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="de822-126">INPUTS</span></span>

### <span data-ttu-id="de822-127">System.String</span><span class="sxs-lookup"><span data-stu-id="de822-127">System.String</span></span>

### <span data-ttu-id="de822-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="de822-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="de822-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="de822-129">OUTPUTS</span></span>

### <span data-ttu-id="de822-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="de822-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="de822-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="de822-131">NOTES</span></span>

## <span data-ttu-id="de822-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="de822-132">RELATED LINKS</span></span>
