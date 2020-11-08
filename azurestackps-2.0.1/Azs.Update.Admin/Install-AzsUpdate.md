---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/install-azsupdate
schema: 2.0.0
ms.openlocfilehash: e6fc8ee19443f0861fb867a5e60d0f637642ff62
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/24/2020
ms.locfileid: "94054290"
---
# <span data-ttu-id="a0420-101">Install-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="a0420-101">Install-AzsUpdate</span></span>

## <span data-ttu-id="a0420-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a0420-102">SYNOPSIS</span></span>
<span data-ttu-id="a0420-103">Stosowanie określonej aktualizacji w lokalizacji aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="a0420-103">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="a0420-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a0420-104">SYNTAX</span></span>

### <span data-ttu-id="a0420-105">Zastosuj (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="a0420-105">Apply (Default)</span></span>
```
Install-AzsUpdate -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a0420-106">ApplyViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a0420-106">ApplyViaIdentity</span></span>
```
Install-AzsUpdate -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a0420-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a0420-107">DESCRIPTION</span></span>
<span data-ttu-id="a0420-108">Stosowanie określonej aktualizacji w lokalizacji aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="a0420-108">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="a0420-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a0420-109">EXAMPLES</span></span>

### <span data-ttu-id="a0420-110">Przykład 1: Install-AzsUpdate według nazwy</span><span class="sxs-lookup"><span data-stu-id="a0420-110">Example 1: Install-AzsUpdate By Name</span></span>
```powershell
PS C:\> Install-AzsUpdate -Name Microsoft1.1907.0.10
```

<span data-ttu-id="a0420-111">Unifiedgroup pozwala instalować określone aktualizacje według nazwy.</span><span class="sxs-lookup"><span data-stu-id="a0420-111">Commandlet allows you to install specific updates by name.</span></span>
<span data-ttu-id="a0420-112">Pamiętaj, że istnieje wymóg, aby wersja aktualizacji była ściśle większa niż bieżąca wersja.</span><span class="sxs-lookup"><span data-stu-id="a0420-112">Note that there is a requirement that the update version is strictly greater than the current version.</span></span>

## <span data-ttu-id="a0420-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a0420-113">PARAMETERS</span></span>

### <span data-ttu-id="a0420-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a0420-114">-AsJob</span></span>
<span data-ttu-id="a0420-115">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="a0420-115">Run the command as a job</span></span>

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

### <span data-ttu-id="a0420-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0420-116">-DefaultProfile</span></span>
<span data-ttu-id="a0420-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a0420-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0420-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a0420-118">-InputObject</span></span>
<span data-ttu-id="a0420-119">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="a0420-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity
Parameter Sets: ApplyViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="a0420-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a0420-120">-Location</span></span>
<span data-ttu-id="a0420-121">Nazwa lokalizacji aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="a0420-121">The name of the update location.</span></span>

```yaml
Type: System.String
Parameter Sets: Apply
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a0420-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a0420-122">-Name</span></span>
<span data-ttu-id="a0420-123">Nazwa aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="a0420-123">Name of the update.</span></span>

```yaml
Type: System.String
Parameter Sets: Apply
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a0420-124">-Nowait</span><span class="sxs-lookup"><span data-stu-id="a0420-124">-NoWait</span></span>
<span data-ttu-id="a0420-125">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="a0420-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a0420-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0420-126">-ResourceGroupName</span></span>
<span data-ttu-id="a0420-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a0420-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Apply
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a0420-128">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="a0420-128">-SubscriptionId</span></span>
<span data-ttu-id="a0420-129">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a0420-129">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a0420-130">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="a0420-130">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Apply
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a0420-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a0420-131">-Confirm</span></span>
<span data-ttu-id="a0420-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0420-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0420-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0420-133">-WhatIf</span></span>
<span data-ttu-id="a0420-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0420-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0420-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a0420-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0420-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0420-136">CommonParameters</span></span>
<span data-ttu-id="a0420-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0420-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0420-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a0420-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0420-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a0420-139">INPUTS</span></span>

### <span data-ttu-id="a0420-140">Microsoft. Azure. PowerShell. polecenia. UpdateAdmin. models. IUpdateAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="a0420-140">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="a0420-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a0420-141">OUTPUTS</span></span>

### <span data-ttu-id="a0420-142">Microsoft. Azure. PowerShell. polecenia. UpdateAdmin. models. Api20160501. IUpdateRun</span><span class="sxs-lookup"><span data-stu-id="a0420-142">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.Api20160501.IUpdateRun</span></span>



## <span data-ttu-id="a0420-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a0420-143">NOTES</span></span>

<span data-ttu-id="a0420-144">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="a0420-144">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a0420-145">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a0420-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="a0420-146">INPUTobject <IUpdateAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="a0420-146">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a0420-147">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="a0420-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a0420-148">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a0420-148">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="a0420-149">`[RunName <String>]`: Identyfikator uruchomienia aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="a0420-149">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="a0420-150">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a0420-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="a0420-151">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="a0420-151">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="a0420-152">`[UpdateLocation <String>]`: Nazwa lokalizacji aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="a0420-152">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="a0420-153">`[UpdateName <String>]`: Nazwa aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="a0420-153">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="a0420-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a0420-154">RELATED LINKS</span></span>

