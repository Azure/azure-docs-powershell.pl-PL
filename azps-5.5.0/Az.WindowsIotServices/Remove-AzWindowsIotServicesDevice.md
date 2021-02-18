---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.windowsiotservices/remove-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Remove-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Remove-AzWindowsIotServicesDevice.md
ms.openlocfilehash: 265c0e68dd3f19afbefd8cf993e058f56e3ec9f3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241467"
---
# <span data-ttu-id="c3b06-101">Remove-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="c3b06-101">Remove-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="c3b06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3b06-102">SYNOPSIS</span></span>
<span data-ttu-id="c3b06-103">Usuń usługę urządzenia z systemem Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="c3b06-103">Delete a Windows IoT Device Service.</span></span>

## <span data-ttu-id="c3b06-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c3b06-104">SYNTAX</span></span>

### <span data-ttu-id="c3b06-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="c3b06-105">Delete (Default)</span></span>
```
Remove-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c3b06-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c3b06-106">DeleteViaIdentity</span></span>
```
Remove-AzWindowsIotServicesDevice -InputObject <IWindowsIotServicesIdentity> [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c3b06-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="c3b06-107">DESCRIPTION</span></span>
<span data-ttu-id="c3b06-108">Usuń usługę urządzenia z systemem Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="c3b06-108">Delete a Windows IoT Device Service.</span></span>

## <span data-ttu-id="c3b06-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c3b06-109">EXAMPLES</span></span>

### <span data-ttu-id="c3b06-110">Przykład 1. Usuwanie usług IoT systemu Windows według nazwy</span><span class="sxs-lookup"><span data-stu-id="c3b06-110">Example 1: Remove a Windows IoT services by name</span></span>
```powershell
PS C:\> Remove-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test

```

<span data-ttu-id="c3b06-111">To polecenie usuwa z nazwy usługi IoT systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="c3b06-111">This command removes a Windows IoT services by name.</span></span>

### <span data-ttu-id="c3b06-112">Przykład 2. Usuwanie usług IoT systemu Windows według potoku</span><span class="sxs-lookup"><span data-stu-id="c3b06-112">Example 2: Remove a Windows IoT services by pipeline</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -ResourceGroupName azure-rg-test -Name wsi-t01 | Remove-AzWindowsIotServicesDevice


```

<span data-ttu-id="c3b06-113">To polecenie usuwa usługi IoT systemu Windows według potoku.</span><span class="sxs-lookup"><span data-stu-id="c3b06-113">This command removes a Windows IoT services by pipeline.</span></span>

## <span data-ttu-id="c3b06-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c3b06-114">PARAMETERS</span></span>

### <span data-ttu-id="c3b06-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3b06-115">-DefaultProfile</span></span>
<span data-ttu-id="c3b06-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c3b06-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3b06-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c3b06-117">-InputObject</span></span>
<span data-ttu-id="c3b06-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="c3b06-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3b06-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c3b06-119">-Name</span></span>
<span data-ttu-id="c3b06-120">Nazwa usługi urządzeń z systemem Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="c3b06-120">The name of the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3b06-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3b06-121">-ResourceGroupName</span></span>
<span data-ttu-id="c3b06-122">Nazwa grupy zasobów zawierającej usługę urządzeń IoT systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="c3b06-122">The name of the resource group that contains the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3b06-123">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c3b06-123">-SubscriptionId</span></span>
<span data-ttu-id="c3b06-124">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="c3b06-124">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3b06-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c3b06-125">-Confirm</span></span>
<span data-ttu-id="c3b06-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c3b06-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3b06-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3b06-127">-WhatIf</span></span>
<span data-ttu-id="c3b06-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3b06-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3b06-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c3b06-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3b06-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3b06-130">CommonParameters</span></span>
<span data-ttu-id="c3b06-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3b06-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3b06-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c3b06-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3b06-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c3b06-133">INPUTS</span></span>

### <span data-ttu-id="c3b06-134">Microsoft.Azure.PowerShell.Cmdlet.WindowsIotServices.Models.IWindowsIotServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="c3b06-134">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span></span>

## <span data-ttu-id="c3b06-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c3b06-135">OUTPUTS</span></span>

### <span data-ttu-id="c3b06-136">Microsoft.Azure.PowerShell.Cmdlet.WindowsIotServices.Models.Api20190601.IDeviceService</span><span class="sxs-lookup"><span data-stu-id="c3b06-136">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="c3b06-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c3b06-137">NOTES</span></span>

<span data-ttu-id="c3b06-138">ALIASY</span><span class="sxs-lookup"><span data-stu-id="c3b06-138">ALIASES</span></span>

<span data-ttu-id="c3b06-139">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c3b06-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c3b06-140">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="c3b06-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c3b06-141">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c3b06-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c3b06-142">INPUTOBJECT: <IWindowsIotServicesIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="c3b06-142">INPUTOBJECT <IWindowsIotServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c3b06-143">`[DeviceName <String>]`: nazwa usługi urządzenia z systemem Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="c3b06-143">`[DeviceName <String>]`: The name of the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="c3b06-144">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="c3b06-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c3b06-145">`[ResourceGroupName <String>]`: nazwa grupy zasobów zawierającej usługę urządzeń IoT systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="c3b06-145">`[ResourceGroupName <String>]`: The name of the resource group that contains the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="c3b06-146">`[SubscriptionId <String>]`: Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="c3b06-146">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="c3b06-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c3b06-147">RELATED LINKS</span></span>

