---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSlot.md
ms.openlocfilehash: 88eaf66ea8584913c7816fd12be19509aec49de5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233720"
---
# <span data-ttu-id="57dba-101">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="57dba-101">Remove-AzWebAppSlot</span></span>

## <span data-ttu-id="57dba-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="57dba-102">SYNOPSIS</span></span>

## <span data-ttu-id="57dba-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="57dba-103">SYNTAX</span></span>

### <span data-ttu-id="57dba-104">S1</span><span class="sxs-lookup"><span data-stu-id="57dba-104">S1</span></span>
```
Remove-AzWebAppSlot [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57dba-105">S2</span><span class="sxs-lookup"><span data-stu-id="57dba-105">S2</span></span>
```
Remove-AzWebAppSlot [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57dba-106">Opis</span><span class="sxs-lookup"><span data-stu-id="57dba-106">DESCRIPTION</span></span>
<span data-ttu-id="57dba-107">Polecenie cmdlet **Remove-AzWebAppSlot** usuwa miejsce w usłudze Azure Web App, pod warunkiem, że grupa zasobów i nazwa aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="57dba-107">The **Remove-AzWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="57dba-108">To polecenie cmdlet domyślnie usuwa także wszystkie gniazda i metryki.</span><span class="sxs-lookup"><span data-stu-id="57dba-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="57dba-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="57dba-109">EXAMPLES</span></span>

### <span data-ttu-id="57dba-110">Przykład 1. Usuń miejsce aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="57dba-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -Slot "Slot001"
```

<span data-ttu-id="57dba-111">To polecenie powoduje usunięcie gniazda o nazwie Slot001 skojarzonego z aplikacją sieci Web ContosoSite należącej do grupy zasobów o nazwie Default-Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="57dba-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="57dba-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="57dba-112">PARAMETERS</span></span>

### <span data-ttu-id="57dba-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="57dba-113">-AsJob</span></span>
<span data-ttu-id="57dba-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="57dba-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57dba-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57dba-115">-DefaultProfile</span></span>
<span data-ttu-id="57dba-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="57dba-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57dba-117">-Force</span><span class="sxs-lookup"><span data-stu-id="57dba-117">-Force</span></span>
<span data-ttu-id="57dba-118">Wymuszone usuwanie opcji</span><span class="sxs-lookup"><span data-stu-id="57dba-118">Forcefully Remove Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57dba-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="57dba-119">-Name</span></span>
<span data-ttu-id="57dba-120">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="57dba-120">WebApp Name</span></span>

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

### <span data-ttu-id="57dba-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57dba-121">-ResourceGroupName</span></span>
<span data-ttu-id="57dba-122">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="57dba-122">Resource Group Name</span></span>

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

### <span data-ttu-id="57dba-123">-Slot</span><span class="sxs-lookup"><span data-stu-id="57dba-123">-Slot</span></span>
<span data-ttu-id="57dba-124">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="57dba-124">WebApp Slot Name</span></span>

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

### <span data-ttu-id="57dba-125">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="57dba-125">-WebApp</span></span>
<span data-ttu-id="57dba-126">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="57dba-126">WebApp Object</span></span>

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

### <span data-ttu-id="57dba-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="57dba-127">-Confirm</span></span>
<span data-ttu-id="57dba-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57dba-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57dba-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57dba-129">-WhatIf</span></span>
<span data-ttu-id="57dba-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57dba-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57dba-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="57dba-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57dba-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57dba-132">CommonParameters</span></span>
<span data-ttu-id="57dba-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57dba-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57dba-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57dba-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57dba-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="57dba-135">INPUTS</span></span>

### <span data-ttu-id="57dba-136">System. String</span><span class="sxs-lookup"><span data-stu-id="57dba-136">System.String</span></span>

### <span data-ttu-id="57dba-137">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="57dba-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="57dba-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="57dba-138">OUTPUTS</span></span>

### <span data-ttu-id="57dba-139">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="57dba-139">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="57dba-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="57dba-140">NOTES</span></span>

## <span data-ttu-id="57dba-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="57dba-141">RELATED LINKS</span></span>

[<span data-ttu-id="57dba-142">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="57dba-142">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="57dba-143">Nowe — AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="57dba-143">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="57dba-144">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="57dba-144">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="57dba-145">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="57dba-145">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="57dba-146">Start — AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="57dba-146">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="57dba-147">Zatrzymaj — AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="57dba-147">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="57dba-148">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="57dba-148">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
