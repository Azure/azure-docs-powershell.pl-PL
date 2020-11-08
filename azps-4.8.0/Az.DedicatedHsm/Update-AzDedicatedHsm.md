---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/update-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Update-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Update-AzDedicatedHsm.md
ms.openlocfilehash: 5aa286eeedb08e6f582210d98a1d29bcd0074031
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062805"
---
# <span data-ttu-id="4bd54-101">Update-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="4bd54-101">Update-AzDedicatedHsm</span></span>

## <span data-ttu-id="4bd54-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4bd54-102">SYNOPSIS</span></span>
<span data-ttu-id="4bd54-103">Aktualizowanie dedykowanego modułu HSM w określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="4bd54-103">Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="4bd54-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4bd54-104">SYNTAX</span></span>

### <span data-ttu-id="4bd54-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4bd54-105">UpdateExpanded (Default)</span></span>
```
Update-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4bd54-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="4bd54-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4bd54-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4bd54-107">DESCRIPTION</span></span>
<span data-ttu-id="4bd54-108">Aktualizowanie dedykowanego modułu HSM w określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="4bd54-108">Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="4bd54-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4bd54-109">EXAMPLES</span></span>

### <span data-ttu-id="4bd54-110">Przykład 1: Aktualizowanie znacznika parametru dedykowanego modułu HSM według nazwy</span><span class="sxs-lookup"><span data-stu-id="4bd54-110">Example 1: Update the parameter tag of the Dedicated HSM by name</span></span>
```powershell
PS C:\> Update-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Tag @{'key1' = '1'; 'key2' = 2; 'key3' = 3}

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="4bd54-111">To polecenie aktualizuje tag parametru dedykowanego modułu HSM według nazwy</span><span class="sxs-lookup"><span data-stu-id="4bd54-111">This command updates the parameter tag of the Dedicated HSM by name</span></span>

### <span data-ttu-id="4bd54-112">Przykład 2: zaktualizowanie znacznika parametru dedykowanego modułu HSM według obiektu</span><span class="sxs-lookup"><span data-stu-id="4bd54-112">Example 2: Update the parameter tag of the Dedicated HSM by object</span></span>
```powershell
PS C:\> $hsm = Get-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz 
PS C:\> Update-AzDedicatedHsm -InputObject -Tag @{'key1' = '1'; 'key2' = 2; 'key3' = 3}

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="4bd54-113">To polecenie aktualizuje tag parametru dedykowanego modułu HSM według obiektu</span><span class="sxs-lookup"><span data-stu-id="4bd54-113">This command updates the parameter tag of the Dedicated HSM by object</span></span>

## <span data-ttu-id="4bd54-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4bd54-114">PARAMETERS</span></span>

### <span data-ttu-id="4bd54-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4bd54-115">-AsJob</span></span>
<span data-ttu-id="4bd54-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="4bd54-116">Run the command as a job</span></span>

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

### <span data-ttu-id="4bd54-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bd54-117">-DefaultProfile</span></span>
<span data-ttu-id="4bd54-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4bd54-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bd54-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4bd54-119">-InputObject</span></span>
<span data-ttu-id="4bd54-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="4bd54-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4bd54-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4bd54-121">-Name</span></span>
<span data-ttu-id="4bd54-122">Nazwa dedykowanego modułu HSM</span><span class="sxs-lookup"><span data-stu-id="4bd54-122">Name of the dedicated HSM</span></span>

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

### <span data-ttu-id="4bd54-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="4bd54-123">-NoWait</span></span>
<span data-ttu-id="4bd54-124">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="4bd54-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4bd54-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bd54-125">-ResourceGroupName</span></span>
<span data-ttu-id="4bd54-126">Nazwa grupy zasobów, do której należy serwer.</span><span class="sxs-lookup"><span data-stu-id="4bd54-126">The name of the Resource Group to which the server belongs.</span></span>

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

### <span data-ttu-id="4bd54-127">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="4bd54-127">-SubscriptionId</span></span>
<span data-ttu-id="4bd54-128">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4bd54-128">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4bd54-129">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="4bd54-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4bd54-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="4bd54-130">-Tag</span></span>
<span data-ttu-id="4bd54-131">Znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="4bd54-131">Resource tags</span></span>

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

### <span data-ttu-id="4bd54-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4bd54-132">-Confirm</span></span>
<span data-ttu-id="4bd54-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4bd54-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bd54-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bd54-134">-WhatIf</span></span>
<span data-ttu-id="4bd54-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4bd54-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bd54-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4bd54-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bd54-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bd54-137">CommonParameters</span></span>
<span data-ttu-id="4bd54-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bd54-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bd54-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4bd54-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bd54-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4bd54-140">INPUTS</span></span>

### <span data-ttu-id="4bd54-141">Microsoft. Azure. PowerShell. polecenia. DedicatedHsm. models. IDedicatedHsmIdentity</span><span class="sxs-lookup"><span data-stu-id="4bd54-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="4bd54-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4bd54-142">OUTPUTS</span></span>

### <span data-ttu-id="4bd54-143">Microsoft. Azure. PowerShell. polecenia. DedicatedHsm. models. Api20181031. IDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="4bd54-143">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="4bd54-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4bd54-144">NOTES</span></span>

<span data-ttu-id="4bd54-145">PISUJE</span><span class="sxs-lookup"><span data-stu-id="4bd54-145">ALIASES</span></span>

<span data-ttu-id="4bd54-146">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4bd54-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4bd54-147">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="4bd54-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4bd54-148">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4bd54-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4bd54-149">INPUTobject <IDedicatedHsmIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="4bd54-149">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4bd54-150">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="4bd54-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4bd54-151">`[Name <String>]`: Nazwa dedykowanego modułu HSM</span><span class="sxs-lookup"><span data-stu-id="4bd54-151">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="4bd54-152">`[ResourceGroupName <String>]`: Nazwa grupy zasobów, do której należy zasób.</span><span class="sxs-lookup"><span data-stu-id="4bd54-152">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="4bd54-153">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4bd54-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="4bd54-154">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="4bd54-154">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="4bd54-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4bd54-155">RELATED LINKS</span></span>

