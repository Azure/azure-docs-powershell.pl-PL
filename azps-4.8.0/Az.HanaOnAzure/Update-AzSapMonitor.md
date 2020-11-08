---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/update-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Update-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Update-AzSapMonitor.md
ms.openlocfilehash: 9d87cfff428a5c3c176bea4deff95d0c652dc45a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220723"
---
# <span data-ttu-id="ce3f1-101">Update-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="ce3f1-101">Update-AzSapMonitor</span></span>

## <span data-ttu-id="ce3f1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ce3f1-102">SYNOPSIS</span></span>
<span data-ttu-id="ce3f1-103">Umożliwia nagrupowanie pola Znaczniki na monitorze SAP dla określonej subskrypcji, grupy zasobów i nazwy monitora.</span><span class="sxs-lookup"><span data-stu-id="ce3f1-103">Patches the Tags field of a SAP monitor for the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="ce3f1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ce3f1-104">SYNTAX</span></span>

### <span data-ttu-id="ce3f1-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ce3f1-105">UpdateExpanded (Default)</span></span>
```
Update-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ce3f1-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ce3f1-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ce3f1-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ce3f1-107">DESCRIPTION</span></span>
<span data-ttu-id="ce3f1-108">Umożliwia nagrupowanie pola Znaczniki na monitorze SAP dla określonej subskrypcji, grupy zasobów i nazwy monitora.</span><span class="sxs-lookup"><span data-stu-id="ce3f1-108">Patches the Tags field of a SAP monitor for the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="ce3f1-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ce3f1-109">EXAMPLES</span></span>

### <span data-ttu-id="ce3f1-110">Przykład 1: aktualizowanie monitora SAP według nazwy</span><span class="sxs-lookup"><span data-stu-id="ce3f1-110">Example 1: Update a SAP monitor by name</span></span>
```powershell
PS C:\> Update-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01 -Tag @{'key'=1;'key2'=2; 'key3'=3}

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="ce3f1-111">To polecenie aktualizuje Monitor protokołu SAP według nazwy.</span><span class="sxs-lookup"><span data-stu-id="ce3f1-111">This commands updates a SAP monitor by name.</span></span>

### <span data-ttu-id="ce3f1-112">Przykład 2: aktualizowanie monitora SAP według obiektów</span><span class="sxs-lookup"><span data-stu-id="ce3f1-112">Example 2: Update a SAP monitor by object</span></span>
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t01
PS C:\> Update-AzSapMonitor -InputObject $sap -Tag @{'key'=1;'key2'=2; 'key3'=3}

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="ce3f1-113">To polecenie aktualizuje Monitor protokołu SAP według obiektu.</span><span class="sxs-lookup"><span data-stu-id="ce3f1-113">This commands updates a SAP monitor by object.</span></span>

## <span data-ttu-id="ce3f1-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ce3f1-114">PARAMETERS</span></span>

### <span data-ttu-id="ce3f1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce3f1-115">-DefaultProfile</span></span>
<span data-ttu-id="ce3f1-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ce3f1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce3f1-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ce3f1-117">-InputObject</span></span>
<span data-ttu-id="ce3f1-118">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="ce3f1-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce3f1-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ce3f1-119">-Name</span></span>
<span data-ttu-id="ce3f1-120">Nazwa zasobu monitorowania protokołu SAP.</span><span class="sxs-lookup"><span data-stu-id="ce3f1-120">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: SapMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce3f1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce3f1-121">-ResourceGroupName</span></span>
<span data-ttu-id="ce3f1-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ce3f1-122">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce3f1-123">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="ce3f1-123">-SubscriptionId</span></span>
<span data-ttu-id="ce3f1-124">Identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ce3f1-124">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ce3f1-125">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="ce3f1-125">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce3f1-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="ce3f1-126">-Tag</span></span>
<span data-ttu-id="ce3f1-127">Pole znaczniki zasobu.</span><span class="sxs-lookup"><span data-stu-id="ce3f1-127">Tags field of the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce3f1-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ce3f1-128">-Confirm</span></span>
<span data-ttu-id="ce3f1-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce3f1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce3f1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce3f1-130">-WhatIf</span></span>
<span data-ttu-id="ce3f1-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce3f1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce3f1-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ce3f1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce3f1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce3f1-133">CommonParameters</span></span>
<span data-ttu-id="ce3f1-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce3f1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce3f1-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ce3f1-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce3f1-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ce3f1-136">INPUTS</span></span>

### <span data-ttu-id="ce3f1-137">Microsoft. Azure. PowerShell. polecenia. HanaOnAzure. models. IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="ce3f1-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="ce3f1-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ce3f1-138">OUTPUTS</span></span>

### <span data-ttu-id="ce3f1-139">Microsoft. Azure. PowerShell. polecenia. HanaOnAzure. models. Api20200207Preview. ISapMonitor</span><span class="sxs-lookup"><span data-stu-id="ce3f1-139">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span></span>

## <span data-ttu-id="ce3f1-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ce3f1-140">NOTES</span></span>

<span data-ttu-id="ce3f1-141">PISUJE</span><span class="sxs-lookup"><span data-stu-id="ce3f1-141">ALIASES</span></span>

<span data-ttu-id="ce3f1-142">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ce3f1-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ce3f1-143">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="ce3f1-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ce3f1-144">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ce3f1-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ce3f1-145">INPUTobject <IHanaOnAzureIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="ce3f1-145">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ce3f1-146">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="ce3f1-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ce3f1-147">`[Location <String>]`: Lokalizacja usuniętego magazynu.</span><span class="sxs-lookup"><span data-stu-id="ce3f1-147">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="ce3f1-148">`[OperationKind <AccessPolicyUpdateKind?>]`: Nazwa operacji</span><span class="sxs-lookup"><span data-stu-id="ce3f1-148">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="ce3f1-149">`[ProviderInstanceName <String>]`: Nazwa wystąpienia dostawcy.</span><span class="sxs-lookup"><span data-stu-id="ce3f1-149">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="ce3f1-150">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ce3f1-150">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="ce3f1-151">`[ResourceName <String>]`: Nazwa zasobu tożsamości.</span><span class="sxs-lookup"><span data-stu-id="ce3f1-151">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="ce3f1-152">`[SapMonitorName <String>]`: Nazwa zasobu monitora SAP.</span><span class="sxs-lookup"><span data-stu-id="ce3f1-152">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="ce3f1-153">`[Scope <String>]`: Zakres zasobu dostawca zasobów.</span><span class="sxs-lookup"><span data-stu-id="ce3f1-153">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="ce3f1-154">Zasób nadrzędny jest rozszerzany przez zarządzane tożsamości.</span><span class="sxs-lookup"><span data-stu-id="ce3f1-154">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="ce3f1-155">`[SubscriptionId <String>]`: Identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ce3f1-155">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ce3f1-156">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="ce3f1-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="ce3f1-157">`[VaultName <String>]`: Nazwa magazynu</span><span class="sxs-lookup"><span data-stu-id="ce3f1-157">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="ce3f1-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ce3f1-158">RELATED LINKS</span></span>

