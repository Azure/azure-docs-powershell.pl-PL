---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/remove-azsnetworkquota
schema: 2.0.0
ms.openlocfilehash: fe7c391b8f15e3389a9d61070b8f55d47af6d6ec
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891674"
---
# <span data-ttu-id="e81d0-101">Remove-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="e81d0-101">Remove-AzsNetworkQuota</span></span>

## <span data-ttu-id="e81d0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e81d0-102">SYNOPSIS</span></span>
<span data-ttu-id="e81d0-103">Usuwanie przydziału według nazwy.</span><span class="sxs-lookup"><span data-stu-id="e81d0-103">Delete a quota by name.</span></span>

## <span data-ttu-id="e81d0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e81d0-104">SYNTAX</span></span>

### <span data-ttu-id="e81d0-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="e81d0-105">Delete (Default)</span></span>
```
Remove-AzsNetworkQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e81d0-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e81d0-106">DeleteViaIdentity</span></span>
```
Remove-AzsNetworkQuota -InputObject <INetworkAdminIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e81d0-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e81d0-107">DESCRIPTION</span></span>
<span data-ttu-id="e81d0-108">Usuwanie przydziału według nazwy.</span><span class="sxs-lookup"><span data-stu-id="e81d0-108">Delete a quota by name.</span></span>

## <span data-ttu-id="e81d0-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e81d0-109">EXAMPLES</span></span>

### <span data-ttu-id="e81d0-110">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e81d0-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="e81d0-111">Usuwanie przydziału sieciowego według nazwy.</span><span class="sxs-lookup"><span data-stu-id="e81d0-111">Remove a network quota by name.</span></span>

### <span data-ttu-id="e81d0-112">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="e81d0-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1 | Remove-AzsNetworkQuota
```

<span data-ttu-id="e81d0-113">Usuwanie przydziału sieci za pomocą potoku.</span><span class="sxs-lookup"><span data-stu-id="e81d0-113">Remove a network quota using a pipe.</span></span>

### <span data-ttu-id="e81d0-114">--------------------------PRZYKŁAD 3--------------------------</span><span class="sxs-lookup"><span data-stu-id="e81d0-114">-------------------------- EXAMPLE 3 --------------------------</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="e81d0-115">Usuwanie przydziału sieci.</span><span class="sxs-lookup"><span data-stu-id="e81d0-115">Remove a network quota.</span></span>

## <span data-ttu-id="e81d0-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e81d0-116">PARAMETERS</span></span>

### <span data-ttu-id="e81d0-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e81d0-117">-AsJob</span></span>
<span data-ttu-id="e81d0-118">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="e81d0-118">Run the command as a job</span></span>

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

### <span data-ttu-id="e81d0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e81d0-119">-DefaultProfile</span></span>
<span data-ttu-id="e81d0-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e81d0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e81d0-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e81d0-121">-InputObject</span></span>
<span data-ttu-id="e81d0-122">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="e81d0-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="e81d0-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e81d0-123">-Location</span></span>
<span data-ttu-id="e81d0-124">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="e81d0-124">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Name
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e81d0-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e81d0-125">-Name</span></span>
<span data-ttu-id="e81d0-126">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="e81d0-126">Name of the resource.</span></span>

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

### <span data-ttu-id="e81d0-127">-Nowait</span><span class="sxs-lookup"><span data-stu-id="e81d0-127">-NoWait</span></span>
<span data-ttu-id="e81d0-128">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="e81d0-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e81d0-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e81d0-129">-PassThru</span></span>
<span data-ttu-id="e81d0-130">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="e81d0-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e81d0-131">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="e81d0-131">-SubscriptionId</span></span>
<span data-ttu-id="e81d0-132">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e81d0-132">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e81d0-133">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="e81d0-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e81d0-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e81d0-134">-Confirm</span></span>
<span data-ttu-id="e81d0-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e81d0-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e81d0-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e81d0-136">-WhatIf</span></span>
<span data-ttu-id="e81d0-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e81d0-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e81d0-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e81d0-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e81d0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e81d0-139">CommonParameters</span></span>
<span data-ttu-id="e81d0-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e81d0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e81d0-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e81d0-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e81d0-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e81d0-142">INPUTS</span></span>

### <span data-ttu-id="e81d0-143">Microsoft. Azure. PowerShell. polecenia. NetworkAdmin. models. INetworkAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="e81d0-143">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity</span></span>

## <span data-ttu-id="e81d0-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e81d0-144">OUTPUTS</span></span>

### <span data-ttu-id="e81d0-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e81d0-145">System.Boolean</span></span>



## <span data-ttu-id="e81d0-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e81d0-146">NOTES</span></span>

<span data-ttu-id="e81d0-147">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="e81d0-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e81d0-148">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e81d0-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="e81d0-149">INPUTobject <INetworkAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="e81d0-149">INPUTOBJECT <INetworkAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e81d0-150">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="e81d0-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e81d0-151">`[Location <String>]`: Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="e81d0-151">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="e81d0-152">`[ResourceName <String>]`: Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="e81d0-152">`[ResourceName <String>]`: Name of the resource.</span></span>
  - <span data-ttu-id="e81d0-153">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e81d0-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e81d0-154">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="e81d0-154">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="e81d0-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e81d0-155">RELATED LINKS</span></span>

