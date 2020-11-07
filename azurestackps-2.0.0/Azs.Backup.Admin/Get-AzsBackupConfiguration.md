---
external help file: ''
Module Name: Azs.Backup.Admin
online version: https://docs.microsoft.com/powershell/module/azs.backup.admin/get-azsbackupconfiguration
schema: 2.0.0
ms.openlocfilehash: 3a9fedc637f8400b952d823a98dfe0abaa1d40d3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93894061"
---
# <span data-ttu-id="a21bf-101">Get-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="a21bf-101">Get-AzsBackupConfiguration</span></span>

## <span data-ttu-id="a21bf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a21bf-102">SYNOPSIS</span></span>
<span data-ttu-id="a21bf-103">Zwraca określoną lokalizację kopii zapasowej na podstawie nazwy.</span><span class="sxs-lookup"><span data-stu-id="a21bf-103">Returns a specific backup location based on name.</span></span>

## <span data-ttu-id="a21bf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a21bf-104">SYNTAX</span></span>

### <span data-ttu-id="a21bf-105">Get (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="a21bf-105">Get (Default)</span></span>
```
Get-AzsBackupConfiguration [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a21bf-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a21bf-106">GetViaIdentity</span></span>
```
Get-AzsBackupConfiguration -InputObject <IBackupAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="a21bf-107">Lista</span><span class="sxs-lookup"><span data-stu-id="a21bf-107">List</span></span>
```
Get-AzsBackupConfiguration [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Skip <String>]
 [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a21bf-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a21bf-108">DESCRIPTION</span></span>
<span data-ttu-id="a21bf-109">Zwraca określoną lokalizację kopii zapasowej na podstawie nazwy.</span><span class="sxs-lookup"><span data-stu-id="a21bf-109">Returns a specific backup location based on name.</span></span>

## <span data-ttu-id="a21bf-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a21bf-110">EXAMPLES</span></span>

### <span data-ttu-id="a21bf-111">Przykład 1: Get-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="a21bf-111">Example 1: Get-AzsBackupConfiguration</span></span>
```powershell
PS C:\> Get-AzsBackupConfiguration

```

<span data-ttu-id="a21bf-112">Pobierz konfigurację kopii zapasowej stosu Azure.</span><span class="sxs-lookup"><span data-stu-id="a21bf-112">Get Azure Stack backup configuration.</span></span>

## <span data-ttu-id="a21bf-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a21bf-113">PARAMETERS</span></span>

### <span data-ttu-id="a21bf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a21bf-114">-DefaultProfile</span></span>
<span data-ttu-id="a21bf-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a21bf-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a21bf-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a21bf-116">-InputObject</span></span>
<span data-ttu-id="a21bf-117">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="a21bf-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a21bf-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a21bf-118">-Location</span></span>
<span data-ttu-id="a21bf-119">Nazwa lokalizacji kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="a21bf-119">Name of the backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a21bf-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a21bf-120">-ResourceGroupName</span></span>
<span data-ttu-id="a21bf-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a21bf-121">Name of the resource group.</span></span>

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

### <span data-ttu-id="a21bf-122">-Skip</span><span class="sxs-lookup"><span data-stu-id="a21bf-122">-Skip</span></span>
<span data-ttu-id="a21bf-123">Parametr pomijania OData.</span><span class="sxs-lookup"><span data-stu-id="a21bf-123">OData skip parameter.</span></span>

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

### <span data-ttu-id="a21bf-124">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="a21bf-124">-SubscriptionId</span></span>
<span data-ttu-id="a21bf-125">Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a21bf-125">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a21bf-126">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="a21bf-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a21bf-127">-Początek</span><span class="sxs-lookup"><span data-stu-id="a21bf-127">-Top</span></span>
<span data-ttu-id="a21bf-128">Parametr najwyższy OData.</span><span class="sxs-lookup"><span data-stu-id="a21bf-128">OData top parameter.</span></span>

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

### <span data-ttu-id="a21bf-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a21bf-129">CommonParameters</span></span>
<span data-ttu-id="a21bf-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a21bf-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a21bf-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a21bf-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a21bf-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a21bf-132">INPUTS</span></span>

### <span data-ttu-id="a21bf-133">Microsoft. Azure. PowerShell. polecenia. BackupAdmin. models. IBackupAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="a21bf-133">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity</span></span>

## <span data-ttu-id="a21bf-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a21bf-134">OUTPUTS</span></span>

### <span data-ttu-id="a21bf-135">Microsoft. Azure. PowerShell. polecenia. BackupAdmin. models. Api20180901. IBackupLocation</span><span class="sxs-lookup"><span data-stu-id="a21bf-135">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackupLocation</span></span>

## <span data-ttu-id="a21bf-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a21bf-136">NOTES</span></span>

<span data-ttu-id="a21bf-137">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="a21bf-137">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a21bf-138">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a21bf-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="a21bf-139">INPUTobject <IBackupAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="a21bf-139">INPUTOBJECT <IBackupAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a21bf-140">`[Backup <String>]`: Nazwa kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="a21bf-140">`[Backup <String>]`: Name of the backup.</span></span>
  - <span data-ttu-id="a21bf-141">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="a21bf-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a21bf-142">`[Location <String>]`: Nazwa lokalizacji kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="a21bf-142">`[Location <String>]`: Name of the backup location.</span></span>
  - <span data-ttu-id="a21bf-143">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a21bf-143">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="a21bf-144">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a21bf-144">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a21bf-145">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="a21bf-145">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="a21bf-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a21bf-146">RELATED LINKS</span></span>

