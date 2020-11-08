---
external help file: ''
Module Name: Azs.Backup.Admin
online version: https://docs.microsoft.com/powershell/module/azs.backup.admin/get-azsbackup
schema: 2.0.0
ms.openlocfilehash: 2c2d517da3be62ff407ca17577edefcf7322ad55
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/24/2020
ms.locfileid: "94054321"
---
# <span data-ttu-id="8ddcc-101">Get-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="8ddcc-101">Get-AzsBackup</span></span>

## <span data-ttu-id="8ddcc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8ddcc-102">SYNOPSIS</span></span>
<span data-ttu-id="8ddcc-103">Zwraca kopię zapasową z lokalizacji na podstawie nazwy.</span><span class="sxs-lookup"><span data-stu-id="8ddcc-103">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="8ddcc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8ddcc-104">SYNTAX</span></span>

### <span data-ttu-id="8ddcc-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="8ddcc-105">List (Default)</span></span>
```
Get-AzsBackup [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Skip <String>]
 [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8ddcc-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="8ddcc-106">Get</span></span>
```
Get-AzsBackup -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8ddcc-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8ddcc-107">GetViaIdentity</span></span>
```
Get-AzsBackup -InputObject <IBackupAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="8ddcc-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8ddcc-108">DESCRIPTION</span></span>
<span data-ttu-id="8ddcc-109">Zwraca kopię zapasową z lokalizacji na podstawie nazwy.</span><span class="sxs-lookup"><span data-stu-id="8ddcc-109">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="8ddcc-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8ddcc-110">EXAMPLES</span></span>

### <span data-ttu-id="8ddcc-111">Przykład 1: kopie zapasowe list</span><span class="sxs-lookup"><span data-stu-id="8ddcc-111">Example 1: List Backups</span></span>
```powershell
PS C:\> Get-AzsBackup

```

<span data-ttu-id="8ddcc-112">Pobierz informacje sbout wszystkie kopie zapasowe stosu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8ddcc-112">Get information sbout all Azure Stack backups.</span></span>

### <span data-ttu-id="8ddcc-113">Przykład 2: pobieranie określonej kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="8ddcc-113">Example 2: Get specific backup</span></span>
```powershell
PS C:\> Get-AzsBackup -Name 'backupName'

```

<span data-ttu-id="8ddcc-114">Uzyskiwanie informacji na temat określonej kopii zapasowej stosu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8ddcc-114">Get information for the the specified Azure Stack backup.</span></span>

## <span data-ttu-id="8ddcc-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8ddcc-115">PARAMETERS</span></span>

### <span data-ttu-id="8ddcc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ddcc-116">-DefaultProfile</span></span>
<span data-ttu-id="8ddcc-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8ddcc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ddcc-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8ddcc-118">-InputObject</span></span>
<span data-ttu-id="8ddcc-119">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="8ddcc-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="8ddcc-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="8ddcc-120">-Location</span></span>
<span data-ttu-id="8ddcc-121">Nazwa lokalizacji kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="8ddcc-121">Name of the backup location.</span></span>

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

### <span data-ttu-id="8ddcc-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8ddcc-122">-Name</span></span>
<span data-ttu-id="8ddcc-123">Nazwa kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="8ddcc-123">Name of the backup.</span></span>

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

### <span data-ttu-id="8ddcc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ddcc-124">-ResourceGroupName</span></span>
<span data-ttu-id="8ddcc-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8ddcc-125">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: "system.$((Get-AzLocation)[0].Location)"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8ddcc-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="8ddcc-126">-Skip</span></span>
<span data-ttu-id="8ddcc-127">Parametr pomijania OData.</span><span class="sxs-lookup"><span data-stu-id="8ddcc-127">OData skip parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8ddcc-128">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="8ddcc-128">-SubscriptionId</span></span>
<span data-ttu-id="8ddcc-129">Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8ddcc-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8ddcc-130">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="8ddcc-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8ddcc-131">-Początek</span><span class="sxs-lookup"><span data-stu-id="8ddcc-131">-Top</span></span>
<span data-ttu-id="8ddcc-132">Parametr najwyższy OData.</span><span class="sxs-lookup"><span data-stu-id="8ddcc-132">OData top parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8ddcc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ddcc-133">CommonParameters</span></span>
<span data-ttu-id="8ddcc-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ddcc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ddcc-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8ddcc-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ddcc-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8ddcc-136">INPUTS</span></span>

### <span data-ttu-id="8ddcc-137">Microsoft. Azure. PowerShell. polecenia. BackupAdmin. models. IBackupAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="8ddcc-137">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity</span></span>

## <span data-ttu-id="8ddcc-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8ddcc-138">OUTPUTS</span></span>

### <span data-ttu-id="8ddcc-139">Microsoft. Azure. PowerShell. polecenia. BackupAdmin. models. Api20180901. IBackup</span><span class="sxs-lookup"><span data-stu-id="8ddcc-139">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackup</span></span>



## <span data-ttu-id="8ddcc-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8ddcc-140">NOTES</span></span>

<span data-ttu-id="8ddcc-141">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="8ddcc-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8ddcc-142">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8ddcc-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="8ddcc-143">INPUTobject <IBackupAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="8ddcc-143">INPUTOBJECT <IBackupAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8ddcc-144">`[Backup <String>]`: Nazwa kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="8ddcc-144">`[Backup <String>]`: Name of the backup.</span></span>
  - <span data-ttu-id="8ddcc-145">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="8ddcc-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8ddcc-146">`[Location <String>]`: Nazwa lokalizacji kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="8ddcc-146">`[Location <String>]`: Name of the backup location.</span></span>
  - <span data-ttu-id="8ddcc-147">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8ddcc-147">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="8ddcc-148">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8ddcc-148">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="8ddcc-149">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="8ddcc-149">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="8ddcc-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8ddcc-150">RELATED LINKS</span></span>

