---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/resume-azsupdaterun
schema: 2.0.0
ms.openlocfilehash: 65d2b3a045d38435cdd709d47c0be88f7fc98af0
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055711"
---
# <span data-ttu-id="7510a-101">Resume-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="7510a-101">Resume-AzsUpdateRun</span></span>

## <span data-ttu-id="7510a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7510a-102">SYNOPSIS</span></span>
<span data-ttu-id="7510a-103">Wznowienie nieudanej aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="7510a-103">Resume a failed update.</span></span>

## <span data-ttu-id="7510a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7510a-104">SYNTAX</span></span>

### <span data-ttu-id="7510a-105">Uruchom ponownie (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="7510a-105">Rerun (Default)</span></span>
```
Resume-AzsUpdateRun -Name <String> -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7510a-106">RerunViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7510a-106">RerunViaIdentity</span></span>
```
Resume-AzsUpdateRun -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7510a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7510a-107">DESCRIPTION</span></span>
<span data-ttu-id="7510a-108">Wznowienie nieudanej aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="7510a-108">Resume a failed update.</span></span>

## <span data-ttu-id="7510a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7510a-109">EXAMPLES</span></span>

### <span data-ttu-id="7510a-110">Przykład 1: Resume-AzsUpdateRun według nazwy i aktualizacji</span><span class="sxs-lookup"><span data-stu-id="7510a-110">Example 1: Resume-AzsUpdateRun By Name and UpdateName</span></span>
```powershell
PS C:\> Resume-AzsUpdateRun -UpdateName northwest/Microsoft1.1907.0.10 -Name 45aaeb26-805b-495b-9c8c-d5da5542dbf4

```

<span data-ttu-id="7510a-111">Unifiedgroup umożliwia ponowne uruchomienie określonego nieudanego procesu aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="7510a-111">Commandlet allows you to rerun a specific failed update run.</span></span>
<span data-ttu-id="7510a-112">Pamiętaj, że istnieje wymóg, aby wersja aktualizacji była ściśle większa niż bieżąca wersja.</span><span class="sxs-lookup"><span data-stu-id="7510a-112">Note that there is a requirement that the update version is strictly greater than the current version.</span></span>

## <span data-ttu-id="7510a-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7510a-113">PARAMETERS</span></span>

### <span data-ttu-id="7510a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7510a-114">-DefaultProfile</span></span>
<span data-ttu-id="7510a-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7510a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7510a-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7510a-116">-InputObject</span></span>
<span data-ttu-id="7510a-117">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="7510a-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity
Parameter Sets: RerunViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="7510a-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="7510a-118">-Location</span></span>
<span data-ttu-id="7510a-119">Nazwa lokalizacji aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="7510a-119">The name of the update location.</span></span>

```yaml
Type: System.String
Parameter Sets: Rerun
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7510a-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7510a-120">-Name</span></span>
<span data-ttu-id="7510a-121">Identyfikator uruchomienia aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="7510a-121">Update run identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Rerun
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7510a-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7510a-122">-PassThru</span></span>
<span data-ttu-id="7510a-123">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="7510a-123">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="7510a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7510a-124">-ResourceGroupName</span></span>
<span data-ttu-id="7510a-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7510a-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Rerun
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7510a-126">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="7510a-126">-SubscriptionId</span></span>
<span data-ttu-id="7510a-127">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7510a-127">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="7510a-128">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="7510a-128">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Rerun
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7510a-129">-Updatename</span><span class="sxs-lookup"><span data-stu-id="7510a-129">-UpdateName</span></span>
<span data-ttu-id="7510a-130">Nazwa aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="7510a-130">Name of the update.</span></span>

```yaml
Type: System.String
Parameter Sets: Rerun
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7510a-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7510a-131">-Confirm</span></span>
<span data-ttu-id="7510a-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7510a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7510a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7510a-133">-WhatIf</span></span>
<span data-ttu-id="7510a-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7510a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7510a-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7510a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7510a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7510a-136">CommonParameters</span></span>
<span data-ttu-id="7510a-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7510a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7510a-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7510a-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7510a-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7510a-139">INPUTS</span></span>

### <span data-ttu-id="7510a-140">Microsoft. Azure. PowerShell. polecenia. UpdateAdmin. models. IUpdateAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="7510a-140">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="7510a-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7510a-141">OUTPUTS</span></span>

### <span data-ttu-id="7510a-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7510a-142">System.Boolean</span></span>



## <span data-ttu-id="7510a-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7510a-143">NOTES</span></span>

<span data-ttu-id="7510a-144">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="7510a-144">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7510a-145">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7510a-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="7510a-146">INPUTobject <IUpdateAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="7510a-146">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7510a-147">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="7510a-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7510a-148">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7510a-148">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="7510a-149">`[RunName <String>]`: Identyfikator uruchomienia aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="7510a-149">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="7510a-150">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7510a-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="7510a-151">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="7510a-151">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="7510a-152">`[UpdateLocation <String>]`: Nazwa lokalizacji aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="7510a-152">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="7510a-153">`[UpdateName <String>]`: Nazwa aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="7510a-153">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="7510a-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7510a-154">RELATED LINKS</span></span>

