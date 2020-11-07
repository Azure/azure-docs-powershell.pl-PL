---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 0FDDDEE1-CEAD-46DA-A7EB-EE477ED59749
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/start-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebAppSlot.md
ms.openlocfilehash: 0535eee5dcdc3d0e78f95951fddcca9d7b8fff3b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888646"
---
# <span data-ttu-id="875cd-101">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="875cd-101">Start-AzWebAppSlot</span></span>

## <span data-ttu-id="875cd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="875cd-102">SYNOPSIS</span></span>
<span data-ttu-id="875cd-103">Uruchamia miejsce aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="875cd-103">Starts an Azure Web App slot.</span></span>

## <span data-ttu-id="875cd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="875cd-104">SYNTAX</span></span>

### <span data-ttu-id="875cd-105">S1</span><span class="sxs-lookup"><span data-stu-id="875cd-105">S1</span></span>
```
Start-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="875cd-106">S2</span><span class="sxs-lookup"><span data-stu-id="875cd-106">S2</span></span>
```
Start-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="875cd-107">Opis</span><span class="sxs-lookup"><span data-stu-id="875cd-107">DESCRIPTION</span></span>
<span data-ttu-id="875cd-108">Polecenie cmdlet **Start-AzWebAppSlot** uruchamia miejsce aplikacji sieci Web platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="875cd-108">The **Start-AzWebAppSlot** cmdlet starts an Azure Web App Slot.</span></span>

## <span data-ttu-id="875cd-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="875cd-109">EXAMPLES</span></span>

### <span data-ttu-id="875cd-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="875cd-110">Example 1</span></span>
```
PS C:\>Start-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="875cd-111">To polecenie umożliwia uruchomienie gniazda o nazwie Slot001 należącego do aplikacji sieci Web o nazwie ContosoWebApp należącej do grupy zasobów o nazwie Default-Web-zachód.</span><span class="sxs-lookup"><span data-stu-id="875cd-111">This command starts the Slot named Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="875cd-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="875cd-112">PARAMETERS</span></span>

### <span data-ttu-id="875cd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="875cd-113">-DefaultProfile</span></span>
<span data-ttu-id="875cd-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="875cd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="875cd-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="875cd-115">-Name</span></span>
<span data-ttu-id="875cd-116">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="875cd-116">WebApp Name</span></span>

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

### <span data-ttu-id="875cd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="875cd-117">-ResourceGroupName</span></span>
<span data-ttu-id="875cd-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="875cd-118">Resource Group Name</span></span>

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

### <span data-ttu-id="875cd-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="875cd-119">-Slot</span></span>
<span data-ttu-id="875cd-120">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="875cd-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="875cd-121">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="875cd-121">-WebApp</span></span>
<span data-ttu-id="875cd-122">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="875cd-122">WebApp Object</span></span>

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

### <span data-ttu-id="875cd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="875cd-123">CommonParameters</span></span>
<span data-ttu-id="875cd-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="875cd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="875cd-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="875cd-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="875cd-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="875cd-126">INPUTS</span></span>

### <span data-ttu-id="875cd-127">System. String</span><span class="sxs-lookup"><span data-stu-id="875cd-127">System.String</span></span>

### <span data-ttu-id="875cd-128">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="875cd-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="875cd-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="875cd-129">OUTPUTS</span></span>

### <span data-ttu-id="875cd-130">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="875cd-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="875cd-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="875cd-131">NOTES</span></span>

## <span data-ttu-id="875cd-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="875cd-132">RELATED LINKS</span></span>

[<span data-ttu-id="875cd-133">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="875cd-133">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="875cd-134">Nowe — AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="875cd-134">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="875cd-135">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="875cd-135">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="875cd-136">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="875cd-136">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="875cd-137">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="875cd-137">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="875cd-138">Zatrzymaj — AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="875cd-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="875cd-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="875cd-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
