---
external help file: ''
Module Name: Azs.Backup.Admin
online version: https://docs.microsoft.com/powershell/module/azs.backup.admin/start-azsbackup
schema: 2.0.0
ms.openlocfilehash: 37fc3ddb1c878bc8b6b1e14d920a5747edce0cd3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93894046"
---
# <span data-ttu-id="94985-101">Start-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="94985-101">Start-AzsBackup</span></span>

## <span data-ttu-id="94985-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="94985-102">SYNOPSIS</span></span>
<span data-ttu-id="94985-103">Wykonaj kopię zapasową określonego miejsca.</span><span class="sxs-lookup"><span data-stu-id="94985-103">Back up a specific location.</span></span>

## <span data-ttu-id="94985-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="94985-104">SYNTAX</span></span>

### <span data-ttu-id="94985-105">Utwórz (domyślne)</span><span class="sxs-lookup"><span data-stu-id="94985-105">Create (Default)</span></span>
```
Start-AzsBackup [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="94985-106">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="94985-106">CreateViaIdentity</span></span>
```
Start-AzsBackup -InputObject <IBackupAdminIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="94985-107">Opis</span><span class="sxs-lookup"><span data-stu-id="94985-107">DESCRIPTION</span></span>
<span data-ttu-id="94985-108">Wykonaj kopię zapasową określonego miejsca.</span><span class="sxs-lookup"><span data-stu-id="94985-108">Back up a specific location.</span></span>

## <span data-ttu-id="94985-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="94985-109">EXAMPLES</span></span>

### <span data-ttu-id="94985-110">Przykład 1: Rozpocznij tworzenie kopii zapasowej azurestack</span><span class="sxs-lookup"><span data-stu-id="94985-110">Example 1: Start azurestack backup</span></span>
```powershell
PS C:\>Start-AzsBackup

```

<span data-ttu-id="94985-111">Rozpocznij tworzenie kopii zapasowej stosu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="94985-111">Start an Azure Stack backup.</span></span>

## <span data-ttu-id="94985-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="94985-112">PARAMETERS</span></span>

### <span data-ttu-id="94985-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="94985-113">-AsJob</span></span>
<span data-ttu-id="94985-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="94985-114">Run the command as a job</span></span>

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

### <span data-ttu-id="94985-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94985-115">-DefaultProfile</span></span>
<span data-ttu-id="94985-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="94985-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94985-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="94985-117">-InputObject</span></span>
<span data-ttu-id="94985-118">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="94985-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity
Parameter Sets: CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="94985-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="94985-119">-Location</span></span>
<span data-ttu-id="94985-120">Nazwa lokalizacji kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="94985-120">Name of the backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: Create
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="94985-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="94985-121">-NoWait</span></span>
<span data-ttu-id="94985-122">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="94985-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="94985-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94985-123">-ResourceGroupName</span></span>
<span data-ttu-id="94985-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="94985-124">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Create
Aliases:

Required: False
Position: Named
Default value: "system.$((Get-AzLocation)[0].Location)"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="94985-125">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="94985-125">-SubscriptionId</span></span>
<span data-ttu-id="94985-126">Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="94985-126">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="94985-127">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="94985-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Create
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="94985-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="94985-128">-Confirm</span></span>
<span data-ttu-id="94985-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94985-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94985-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94985-130">-WhatIf</span></span>
<span data-ttu-id="94985-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94985-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94985-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="94985-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94985-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94985-133">CommonParameters</span></span>
<span data-ttu-id="94985-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94985-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94985-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="94985-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94985-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="94985-136">INPUTS</span></span>

### <span data-ttu-id="94985-137">Microsoft. Azure. PowerShell. polecenia. BackupAdmin. models. IBackupAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="94985-137">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity</span></span>

## <span data-ttu-id="94985-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="94985-138">OUTPUTS</span></span>

### <span data-ttu-id="94985-139">Microsoft. Azure. PowerShell. polecenia. BackupAdmin. models. Api20180901. IBackup</span><span class="sxs-lookup"><span data-stu-id="94985-139">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackup</span></span>



## <span data-ttu-id="94985-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="94985-140">NOTES</span></span>

<span data-ttu-id="94985-141">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="94985-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="94985-142">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="94985-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="94985-143">INPUTobject <IBackupAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="94985-143">INPUTOBJECT <IBackupAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="94985-144">`[Backup <String>]`: Nazwa kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="94985-144">`[Backup <String>]`: Name of the backup.</span></span>
  - <span data-ttu-id="94985-145">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="94985-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="94985-146">`[Location <String>]`: Nazwa lokalizacji kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="94985-146">`[Location <String>]`: Name of the backup location.</span></span>
  - <span data-ttu-id="94985-147">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="94985-147">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="94985-148">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="94985-148">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="94985-149">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="94985-149">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="94985-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="94985-150">RELATED LINKS</span></span>

