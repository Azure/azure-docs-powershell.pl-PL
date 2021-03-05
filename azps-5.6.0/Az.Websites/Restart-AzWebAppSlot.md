---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 645E74D2-640D-494F-9798-4375FE6A0AF2
online version: https://docs.microsoft.com/powershell/module/az.websites/restart-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebAppSlot.md
ms.openlocfilehash: 75bedf4546bee73767c0488f578cdb5e17c1b745
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002081"
---
# <span data-ttu-id="d31f7-101">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d31f7-101">Restart-AzWebAppSlot</span></span>

## <span data-ttu-id="d31f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d31f7-102">SYNOPSIS</span></span>

## <span data-ttu-id="d31f7-103">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d31f7-103">SYNTAX</span></span>

### <span data-ttu-id="d31f7-104">S1</span><span class="sxs-lookup"><span data-stu-id="d31f7-104">S1</span></span>
```
Restart-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d31f7-105">S2</span><span class="sxs-lookup"><span data-stu-id="d31f7-105">S2</span></span>
```
Restart-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d31f7-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="d31f7-106">DESCRIPTION</span></span>
<span data-ttu-id="d31f7-107">Polecenie **cmdlet Restart-AzWebAppSlot** zostanie zatrzymane, a następnie zostanie uruchomione miejsce aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="d31f7-107">The **Restart-AzWebAppSlot** cmdlet stops and then starts an Azure Web App Slot.</span></span>
<span data-ttu-id="d31f7-108">Jeśli miejsce aplikacji sieci Web znajduje się w stanie zatrzymania, użyj Start-AzWebAppSlot cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d31f7-108">If the Web App Slot is in a stopped state, use the Start-AzWebAppSlot cmdlet.</span></span>

## <span data-ttu-id="d31f7-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d31f7-109">EXAMPLES</span></span>

### <span data-ttu-id="d31f7-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d31f7-110">Example 1</span></span>
```
PS C:\> Restart-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="d31f7-111">To polecenie powoduje ponowne uruchomienie gniazda Slot001 dla aplikacji sieci Web ContosoWebApp skojarzonej z grupą zasobów Default-Web-WestUS</span><span class="sxs-lookup"><span data-stu-id="d31f7-111">This command restarts the slot Slot001 for the web app ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="d31f7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d31f7-112">PARAMETERS</span></span>

### <span data-ttu-id="d31f7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d31f7-113">-DefaultProfile</span></span>
<span data-ttu-id="d31f7-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d31f7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d31f7-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d31f7-115">-Name</span></span>
<span data-ttu-id="d31f7-116">Nazwa aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="d31f7-116">WebApp Name</span></span>

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

### <span data-ttu-id="d31f7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d31f7-117">-ResourceGroupName</span></span>
<span data-ttu-id="d31f7-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="d31f7-118">Resource Group Name</span></span>

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

### <span data-ttu-id="d31f7-119">— Slot</span><span class="sxs-lookup"><span data-stu-id="d31f7-119">-Slot</span></span>
<span data-ttu-id="d31f7-120">Nazwa gniazda aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="d31f7-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="d31f7-121">- WebApp</span><span class="sxs-lookup"><span data-stu-id="d31f7-121">-WebApp</span></span>
<span data-ttu-id="d31f7-122">Obiekt WebApp</span><span class="sxs-lookup"><span data-stu-id="d31f7-122">WebApp Object</span></span>

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

### <span data-ttu-id="d31f7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d31f7-123">CommonParameters</span></span>
<span data-ttu-id="d31f7-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d31f7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d31f7-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d31f7-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d31f7-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d31f7-126">INPUTS</span></span>

### <span data-ttu-id="d31f7-127">System.String</span><span class="sxs-lookup"><span data-stu-id="d31f7-127">System.String</span></span>

### <span data-ttu-id="d31f7-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="d31f7-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="d31f7-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d31f7-129">OUTPUTS</span></span>

### <span data-ttu-id="d31f7-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="d31f7-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="d31f7-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d31f7-131">NOTES</span></span>

## <span data-ttu-id="d31f7-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d31f7-132">RELATED LINKS</span></span>

[<span data-ttu-id="d31f7-133">Get-AzWebAppslot</span><span class="sxs-lookup"><span data-stu-id="d31f7-133">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="d31f7-134">New-AzWebAppslot</span><span class="sxs-lookup"><span data-stu-id="d31f7-134">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="d31f7-135">Remove-AzWebAppslot</span><span class="sxs-lookup"><span data-stu-id="d31f7-135">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="d31f7-136">Set-AzWebAppslot</span><span class="sxs-lookup"><span data-stu-id="d31f7-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="d31f7-137">Start-AzWebAppslot</span><span class="sxs-lookup"><span data-stu-id="d31f7-137">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="d31f7-138">Stop-AzWebAppslot</span><span class="sxs-lookup"><span data-stu-id="d31f7-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="d31f7-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d31f7-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
