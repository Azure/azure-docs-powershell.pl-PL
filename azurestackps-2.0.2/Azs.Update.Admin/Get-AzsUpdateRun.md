---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/get-azsupdaterun
schema: 2.0.0
ms.openlocfilehash: fb36cb0d1be46abb66a1c0cc97165f8eb9cc3913
ms.sourcegitcommit: f7edd4f5c4bebedc139cb01438081edc6ed560bd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/29/2020
ms.locfileid: "94061819"
---
# <span data-ttu-id="35d57-101">Get-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="35d57-101">Get-AzsUpdateRun</span></span>

## <span data-ttu-id="35d57-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="35d57-102">SYNOPSIS</span></span>
<span data-ttu-id="35d57-103">Uruchom wystąpienie aktualizacji przy użyciu identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="35d57-103">Get an instance of update run using the ID.</span></span>

## <span data-ttu-id="35d57-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="35d57-104">SYNTAX</span></span>

### <span data-ttu-id="35d57-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="35d57-105">List (Default)</span></span>
```
Get-AzsUpdateRun -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="35d57-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="35d57-106">Get</span></span>
```
Get-AzsUpdateRun -Name <String> -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="35d57-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="35d57-107">GetViaIdentity</span></span>
```
Get-AzsUpdateRun -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="35d57-108">Opis</span><span class="sxs-lookup"><span data-stu-id="35d57-108">DESCRIPTION</span></span>
<span data-ttu-id="35d57-109">Uruchom wystąpienie aktualizacji przy użyciu identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="35d57-109">Get an instance of update run using the ID.</span></span>

## <span data-ttu-id="35d57-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="35d57-110">EXAMPLES</span></span>

### <span data-ttu-id="35d57-111">Przykład 1: Get-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="35d57-111">Example 1: Get-AzsUpdateRun</span></span>
```powershell
PS C:\> Get-AzsUpdateRun

cmdlet Get-AzsUpdateRun at command pipeline position 1
Supply values for the following parameters:
UpdateName: Microsoft1.1907.0.10

Name                                     State           ProgressStartTimeUtc      ProgressEndTimeUtc
----                                     -----           --------------------      ------------------
northwest/Microsoft1.1907.0.10/45aaeb... Failed          7/11/2019 3:07:10 PM      7/11/2019 7:38:05 PM
northwest/Microsoft1.1907.0.10/51e878... Succeeded       7/11/2019 3:07:10 PM      7/12/2019 6:47:37 AM
```

<span data-ttu-id="35d57-112">Jeśli wartość Updatename nie jest określona, Get-UpdateRun będzie zawsze pytać o dane wejściowe.</span><span class="sxs-lookup"><span data-stu-id="35d57-112">If a UpdateName value is not specified, Get-UpdateRun will always ask for input.</span></span>
<span data-ttu-id="35d57-113">Po pomyślnym wyprowadzeniu wszystkich wystąpień UpdateRun, które nie powiodły się lub powiodło się.</span><span class="sxs-lookup"><span data-stu-id="35d57-113">Once provided, it will output all instances of UpdateRun that were Failed or Successful</span></span>

### <span data-ttu-id="35d57-114">Przykład 2: Get-AzsUpdateRun według aktualizacji</span><span class="sxs-lookup"><span data-stu-id="35d57-114">Example 2: Get-AzsUpdateRun By UpdateName</span></span>
```powershell
PS C:\> Get-AzsUpdateRun -UpdateName Microsoft1.1907.0.10
or 
PS C:\> Get-AzsUpdateRun -UpdateName northwest/Microsoft1.1907.0.10

Name                                     State           ProgressStartTimeUtc      ProgressEndTimeUtc
----                                     -----           --------------------      ------------------
northwest/Microsoft1.1907.0.10/45aaeb... Failed          7/11/2019 3:07:10 PM      7/11/2019 7:38:05 PM
northwest/Microsoft1.1907.0.10/51e878... Succeeded       7/11/2019 3:07:10 PM      7/12/2019 6:47:37 AM
```

<span data-ttu-id="35d57-115">Umożliwia pobranie wszystkich UpdateRuns skojarzonych z określoną aktualizacją.</span><span class="sxs-lookup"><span data-stu-id="35d57-115">Will retrieve all UpdateRuns associated with a specific Update</span></span>

### <span data-ttu-id="35d57-116">Przykład 2: Get-AzsUpdateRun według nazwy</span><span class="sxs-lookup"><span data-stu-id="35d57-116">Example 2: Get-AzsUpdateRun By Name</span></span>
```powershell
PS C:\> Get-AzsUpdateRun -UpdateName Microsoft1.1907.0.10 -Name 45aaeb26-805b-495b-9c8c-d5da5542dbf4
or 
PS C:\> Get-AzsUpdateRun -UpdateName northwest/Microsoft1.1907.0.10 -Name northwest/Microsoft1.1907.0.10/45aaeb26-805b-495b-9c8c-d5da5542dbf4

Name                                     State           ProgressStartTimeUtc      ProgressEndTimeUtc
----                                     -----           --------------------      ------------------
northwest/Microsoft1.1907.0.10/45aaeb... Failed          7/11/2019 3:07:10 PM      7/11/2019 7:38:05 PM
```

<span data-ttu-id="35d57-117">Umożliwia pobranie wszystkich UpdateRuns skojarzonych z określoną aktualizacją i określoną nazwą.</span><span class="sxs-lookup"><span data-stu-id="35d57-117">Will retrieve all UpdateRuns associated with a specific Update and a specific Name</span></span>

## <span data-ttu-id="35d57-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="35d57-118">PARAMETERS</span></span>

### <span data-ttu-id="35d57-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35d57-119">-DefaultProfile</span></span>
<span data-ttu-id="35d57-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="35d57-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35d57-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="35d57-121">-InputObject</span></span>
<span data-ttu-id="35d57-122">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="35d57-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="35d57-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="35d57-123">-Location</span></span>
<span data-ttu-id="35d57-124">Nazwa lokalizacji aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="35d57-124">The name of the update location.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="35d57-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="35d57-125">-Name</span></span>
<span data-ttu-id="35d57-126">Identyfikator uruchomienia aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="35d57-126">Update run identifier.</span></span>

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

### <span data-ttu-id="35d57-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35d57-127">-ResourceGroupName</span></span>
<span data-ttu-id="35d57-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="35d57-128">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="35d57-129">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="35d57-129">-SubscriptionId</span></span>
<span data-ttu-id="35d57-130">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="35d57-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="35d57-131">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="35d57-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="35d57-132">-Updatename</span><span class="sxs-lookup"><span data-stu-id="35d57-132">-UpdateName</span></span>
<span data-ttu-id="35d57-133">Nazwa aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="35d57-133">Name of the update.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="35d57-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35d57-134">CommonParameters</span></span>
<span data-ttu-id="35d57-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35d57-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35d57-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35d57-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35d57-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="35d57-137">INPUTS</span></span>

### <span data-ttu-id="35d57-138">Microsoft. Azure. PowerShell. polecenia. UpdateAdmin. models. IUpdateAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="35d57-138">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="35d57-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="35d57-139">OUTPUTS</span></span>

### <span data-ttu-id="35d57-140">Microsoft. Azure. PowerShell. polecenia. UpdateAdmin. models. Api20160501. IUpdateRun</span><span class="sxs-lookup"><span data-stu-id="35d57-140">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.Api20160501.IUpdateRun</span></span>



## <span data-ttu-id="35d57-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="35d57-141">NOTES</span></span>

<span data-ttu-id="35d57-142">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="35d57-142">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="35d57-143">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="35d57-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="35d57-144">INPUTobject <IUpdateAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="35d57-144">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="35d57-145">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="35d57-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="35d57-146">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="35d57-146">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="35d57-147">`[RunName <String>]`: Identyfikator uruchomienia aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="35d57-147">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="35d57-148">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="35d57-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="35d57-149">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="35d57-149">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="35d57-150">`[UpdateLocation <String>]`: Nazwa lokalizacji aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="35d57-150">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="35d57-151">`[UpdateName <String>]`: Nazwa aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="35d57-151">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="35d57-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="35d57-152">RELATED LINKS</span></span>

