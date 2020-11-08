---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/get-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitor.md
ms.openlocfilehash: 1ec82e745c7f6521a62db80ca109078bb1681172
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224313"
---
# <span data-ttu-id="39888-101">Get-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="39888-101">Get-AzSapMonitor</span></span>

## <span data-ttu-id="39888-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="39888-102">SYNOPSIS</span></span>
<span data-ttu-id="39888-103">Pobiera właściwości monitora SAP dla określonej subskrypcji, grupy zasobów i nazwy zasobu.</span><span class="sxs-lookup"><span data-stu-id="39888-103">Gets properties of a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="39888-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="39888-104">SYNTAX</span></span>

### <span data-ttu-id="39888-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="39888-105">List (Default)</span></span>
```
Get-AzSapMonitor [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="39888-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="39888-106">Get</span></span>
```
Get-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="39888-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="39888-107">GetViaIdentity</span></span>
```
Get-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="39888-108">Opis</span><span class="sxs-lookup"><span data-stu-id="39888-108">DESCRIPTION</span></span>
<span data-ttu-id="39888-109">Pobiera właściwości monitora SAP dla określonej subskrypcji, grupy zasobów i nazwy zasobu.</span><span class="sxs-lookup"><span data-stu-id="39888-109">Gets properties of a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="39888-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="39888-110">EXAMPLES</span></span>

### <span data-ttu-id="39888-111">Przykład 1. Uzyskaj wszystkie monitory protokołu SAP w ramach abonamentu</span><span class="sxs-lookup"><span data-stu-id="39888-111">Example 1: Get all SAP monitors under a subscription</span></span>
```powershell
PS C:\> Get-AzSapMonitor

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="39888-112">To polecenie pobiera monitory SAP w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="39888-112">This command gets SAP monitors under a subscription.</span></span>

### <span data-ttu-id="39888-113">Przykład 2: uzyskiwanie monitora SAP według nazwy</span><span class="sxs-lookup"><span data-stu-id="39888-113">Example 2: Get a SAP monitor by name</span></span>
```powershell
PS C:\> Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="39888-114">To polecenie pobiera Monitor protokołu SAP według nazwy.</span><span class="sxs-lookup"><span data-stu-id="39888-114">This command gets a SAP monitor by name.</span></span>

### <span data-ttu-id="39888-115">Przykład 3: uzyskiwanie monitora SAP według obiektów</span><span class="sxs-lookup"><span data-stu-id="39888-115">Example 3: Get a SAP monitor by object</span></span>
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01
PS C:\> Get-AzSapMonitor -InputObject $sap

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="39888-116">To polecenie pobiera Monitor protokołu SAP według obiektu.</span><span class="sxs-lookup"><span data-stu-id="39888-116">This command gets a SAP monitor by object.</span></span>

### <span data-ttu-id="39888-117">Przykład 4: uzyskiwanie monitora SAP według rurociągu</span><span class="sxs-lookup"><span data-stu-id="39888-117">Example 4: Get a SAP monitor by pipeline</span></span>
```powershell
PS C:\> @{Id='/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.HanaOnAzure/sapMonitors/ps-spamonitor-t01'} | Get-AzSapMonitor

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="39888-118">To polecenie pobiera Monitor protokołu SAP według rurociągu.</span><span class="sxs-lookup"><span data-stu-id="39888-118">This command gets a SAP monitor by pipeline.</span></span>

## <span data-ttu-id="39888-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="39888-119">PARAMETERS</span></span>

### <span data-ttu-id="39888-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39888-120">-DefaultProfile</span></span>
<span data-ttu-id="39888-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="39888-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39888-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="39888-122">-InputObject</span></span>
<span data-ttu-id="39888-123">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="39888-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="39888-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="39888-124">-Name</span></span>
<span data-ttu-id="39888-125">Nazwa zasobu monitorowania protokołu SAP.</span><span class="sxs-lookup"><span data-stu-id="39888-125">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: SapMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39888-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39888-126">-ResourceGroupName</span></span>
<span data-ttu-id="39888-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="39888-127">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39888-128">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="39888-128">-SubscriptionId</span></span>
<span data-ttu-id="39888-129">Identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="39888-129">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="39888-130">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="39888-130">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39888-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39888-131">CommonParameters</span></span>
<span data-ttu-id="39888-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39888-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39888-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="39888-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39888-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="39888-134">INPUTS</span></span>

### <span data-ttu-id="39888-135">Microsoft. Azure. PowerShell. polecenia. HanaOnAzure. models. IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="39888-135">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="39888-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="39888-136">OUTPUTS</span></span>

### <span data-ttu-id="39888-137">Microsoft. Azure. PowerShell. polecenia. HanaOnAzure. models. Api20200207Preview. ISapMonitor</span><span class="sxs-lookup"><span data-stu-id="39888-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span></span>

## <span data-ttu-id="39888-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="39888-138">NOTES</span></span>

<span data-ttu-id="39888-139">PISUJE</span><span class="sxs-lookup"><span data-stu-id="39888-139">ALIASES</span></span>

<span data-ttu-id="39888-140">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="39888-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="39888-141">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="39888-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="39888-142">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="39888-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="39888-143">INPUTobject <IHanaOnAzureIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="39888-143">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="39888-144">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="39888-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="39888-145">`[Location <String>]`: Lokalizacja usuniętego magazynu.</span><span class="sxs-lookup"><span data-stu-id="39888-145">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="39888-146">`[OperationKind <AccessPolicyUpdateKind?>]`: Nazwa operacji</span><span class="sxs-lookup"><span data-stu-id="39888-146">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="39888-147">`[ProviderInstanceName <String>]`: Nazwa wystąpienia dostawcy.</span><span class="sxs-lookup"><span data-stu-id="39888-147">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="39888-148">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="39888-148">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="39888-149">`[ResourceName <String>]`: Nazwa zasobu tożsamości.</span><span class="sxs-lookup"><span data-stu-id="39888-149">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="39888-150">`[SapMonitorName <String>]`: Nazwa zasobu monitora SAP.</span><span class="sxs-lookup"><span data-stu-id="39888-150">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="39888-151">`[Scope <String>]`: Zakres zasobu dostawca zasobów.</span><span class="sxs-lookup"><span data-stu-id="39888-151">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="39888-152">Zasób nadrzędny jest rozszerzany przez zarządzane tożsamości.</span><span class="sxs-lookup"><span data-stu-id="39888-152">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="39888-153">`[SubscriptionId <String>]`: Identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="39888-153">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="39888-154">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="39888-154">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="39888-155">`[VaultName <String>]`: Nazwa magazynu</span><span class="sxs-lookup"><span data-stu-id="39888-155">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="39888-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="39888-156">RELATED LINKS</span></span>

