---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.windowsiotservices/remove-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Remove-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Remove-AzWindowsIotServicesDevice.md
ms.openlocfilehash: 265c0e68dd3f19afbefd8cf993e058f56e3ec9f3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491365"
---
# <span data-ttu-id="f49fc-101">Remove-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="f49fc-101">Remove-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="f49fc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f49fc-102">SYNOPSIS</span></span>
<span data-ttu-id="f49fc-103">Usuwanie usługi urządzeń z systemem Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="f49fc-103">Delete a Windows IoT Device Service.</span></span>

## <span data-ttu-id="f49fc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f49fc-104">SYNTAX</span></span>

### <span data-ttu-id="f49fc-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="f49fc-105">Delete (Default)</span></span>
```
Remove-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f49fc-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f49fc-106">DeleteViaIdentity</span></span>
```
Remove-AzWindowsIotServicesDevice -InputObject <IWindowsIotServicesIdentity> [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f49fc-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f49fc-107">DESCRIPTION</span></span>
<span data-ttu-id="f49fc-108">Usuwanie usługi urządzeń z systemem Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="f49fc-108">Delete a Windows IoT Device Service.</span></span>

## <span data-ttu-id="f49fc-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f49fc-109">EXAMPLES</span></span>

### <span data-ttu-id="f49fc-110">Przykład 1: Usuwanie usług IoT systemu Windows według nazw</span><span class="sxs-lookup"><span data-stu-id="f49fc-110">Example 1: Remove a Windows IoT services by name</span></span>
```powershell
PS C:\> Remove-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test

```

<span data-ttu-id="f49fc-111">To polecenie powoduje usunięcie usług IoT systemu Windows według nazwy.</span><span class="sxs-lookup"><span data-stu-id="f49fc-111">This command removes a Windows IoT services by name.</span></span>

### <span data-ttu-id="f49fc-112">Przykład 2: Usuwanie usług IoT systemu Windows według rurociągu</span><span class="sxs-lookup"><span data-stu-id="f49fc-112">Example 2: Remove a Windows IoT services by pipeline</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -ResourceGroupName azure-rg-test -Name wsi-t01 | Remove-AzWindowsIotServicesDevice


```

<span data-ttu-id="f49fc-113">To polecenie usuwa usługi Windows IoT według rurociągu.</span><span class="sxs-lookup"><span data-stu-id="f49fc-113">This command removes a Windows IoT services by pipeline.</span></span>

## <span data-ttu-id="f49fc-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f49fc-114">PARAMETERS</span></span>

### <span data-ttu-id="f49fc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f49fc-115">-DefaultProfile</span></span>
<span data-ttu-id="f49fc-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f49fc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f49fc-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f49fc-117">-InputObject</span></span>
<span data-ttu-id="f49fc-118">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="f49fc-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f49fc-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f49fc-119">-Name</span></span>
<span data-ttu-id="f49fc-120">Nazwa usługi urządzeń z systemem Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="f49fc-120">The name of the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="f49fc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f49fc-121">-ResourceGroupName</span></span>
<span data-ttu-id="f49fc-122">Nazwa grupy zasobów zawierającej usługę urządzenia z usługami IoT systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="f49fc-122">The name of the resource group that contains the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="f49fc-123">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="f49fc-123">-SubscriptionId</span></span>
<span data-ttu-id="f49fc-124">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f49fc-124">The subscription identifier.</span></span>

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

### <span data-ttu-id="f49fc-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f49fc-125">-Confirm</span></span>
<span data-ttu-id="f49fc-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f49fc-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f49fc-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f49fc-127">-WhatIf</span></span>
<span data-ttu-id="f49fc-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f49fc-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f49fc-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f49fc-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f49fc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f49fc-130">CommonParameters</span></span>
<span data-ttu-id="f49fc-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f49fc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f49fc-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f49fc-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f49fc-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f49fc-133">INPUTS</span></span>

### <span data-ttu-id="f49fc-134">Microsoft. Azure. PowerShell. polecenia. WindowsIotServices. models. IWindowsIotServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="f49fc-134">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span></span>

## <span data-ttu-id="f49fc-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f49fc-135">OUTPUTS</span></span>

### <span data-ttu-id="f49fc-136">Microsoft. Azure. PowerShell. polecenia. WindowsIotServices. models. Api20190601. IDeviceService</span><span class="sxs-lookup"><span data-stu-id="f49fc-136">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="f49fc-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f49fc-137">NOTES</span></span>

<span data-ttu-id="f49fc-138">PISUJE</span><span class="sxs-lookup"><span data-stu-id="f49fc-138">ALIASES</span></span>

<span data-ttu-id="f49fc-139">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f49fc-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f49fc-140">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="f49fc-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f49fc-141">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f49fc-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f49fc-142">INPUTobject <IWindowsIotServicesIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="f49fc-142">INPUTOBJECT <IWindowsIotServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f49fc-143">`[DeviceName <String>]`: Nazwa usługi urządzeń z systemem Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="f49fc-143">`[DeviceName <String>]`: The name of the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="f49fc-144">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="f49fc-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f49fc-145">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej usługę urządzeń z systemem Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="f49fc-145">`[ResourceGroupName <String>]`: The name of the resource group that contains the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="f49fc-146">`[SubscriptionId <String>]`: Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f49fc-146">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="f49fc-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f49fc-147">RELATED LINKS</span></span>

