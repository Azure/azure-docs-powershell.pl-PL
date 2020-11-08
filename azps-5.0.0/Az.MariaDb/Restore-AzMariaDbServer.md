---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/restore-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restore-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restore-AzMariaDbServer.md
ms.openlocfilehash: 95988d83cbb4c3dcf0b5da890bf38f8c40eb4dfa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234563"
---
# <span data-ttu-id="6a77f-101">Restore-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="6a77f-101">Restore-AzMariaDbServer</span></span>

## <span data-ttu-id="6a77f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6a77f-102">SYNOPSIS</span></span>
<span data-ttu-id="6a77f-103">Przywróć MariaDB z istniejącej MariaDB.</span><span class="sxs-lookup"><span data-stu-id="6a77f-103">Restore a MariaDB from a existing MariaDB.</span></span>

## <span data-ttu-id="6a77f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6a77f-104">SYNTAX</span></span>

```
Restore-AzMariaDbServer -Name <String> -RestorePointInTime <DateTime> [-InputObject <IServer>]
 [-ResourceGroupName <String>] [-ServerName <String>] [-SubscriptionId <String>] [-Location <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6a77f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6a77f-105">DESCRIPTION</span></span>
<span data-ttu-id="6a77f-106">Przywróć MariaDB z istniejącej MariaDB.</span><span class="sxs-lookup"><span data-stu-id="6a77f-106">Restore a MariaDB from a existing MariaDB.</span></span>

## <span data-ttu-id="6a77f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6a77f-107">EXAMPLES</span></span>

### <span data-ttu-id="6a77f-108">Przykład 1: Przywracanie PointInTime MariaDB według nazwy serwera.</span><span class="sxs-lookup"><span data-stu-id="6a77f-108">Example 1: Restore a PointInTime MariaDB by server name.</span></span>
```powershell
PS C:\> Restore-AzMariaDbServer -Name restore-db01 -ServerName mariadb-test-usegeo -ResourceGroupName mariadb-test-4rih5z -UsePointInTimeRestore -RestorePointInTime $(Get-Date) -Location eastus

Name         Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----         -------- ------------------ ------- ----------------------- -------   -------        --------------
restore-db01 eastus   adminuser          10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="6a77f-109">To polecenie przywraca PointInTime MariaDB według nazwy serwera.</span><span class="sxs-lookup"><span data-stu-id="6a77f-109">This command restore a PointInTime MariaDB by server name.</span></span>

### <span data-ttu-id="6a77f-110">Przykład 2: Przywracanie PointInTime MariaDB według obiektu serwera</span><span class="sxs-lookup"><span data-stu-id="6a77f-110">Example 2: Restore a PointInTime MariaDB by server object</span></span>
```powershell
PS C:\> $db = Get-AzMariaDbServer -Name mariadb-test-usegeo -ResourceGroupName mariadb-test-4rih5z
PS C:\>Restore-AzMariaDbServer -Name restore-db02 -InputObject $db -UsePointInTimeRestore -RestorePointInTime $(Get-Date) -Location eastus

Name         Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----         -------- ------------------ ------- ----------------------- -------   -------        --------------
restore-db02 eastus   adminuser          10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="6a77f-111">To polecenie przywraca PointInTime MariaDB według obiektu serwera.</span><span class="sxs-lookup"><span data-stu-id="6a77f-111">This command restore a PointInTime MariaDB by server object.</span></span>

## <span data-ttu-id="6a77f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6a77f-112">PARAMETERS</span></span>

### <span data-ttu-id="6a77f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6a77f-113">-AsJob</span></span>
<span data-ttu-id="6a77f-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="6a77f-114">Run the command as a job</span></span>

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

### <span data-ttu-id="6a77f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a77f-115">-DefaultProfile</span></span>
<span data-ttu-id="6a77f-116">Region DefaultParameters poświadczenia, konto, dzierżawca i abonament używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6a77f-116">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a77f-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6a77f-117">-InputObject</span></span>
<span data-ttu-id="6a77f-118">Źródłowy obiekt serwera do przywrócenia.</span><span class="sxs-lookup"><span data-stu-id="6a77f-118">The source server object to restore from.</span></span>
<span data-ttu-id="6a77f-119">Aby skonstruować, zobacz sekcję notatki dla właściwości INPUTobject i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="6a77f-119">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a77f-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="6a77f-120">-Location</span></span>
<span data-ttu-id="6a77f-121">Miejsce, w którym znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="6a77f-121">The location the resource resides in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a77f-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6a77f-122">-Name</span></span>
<span data-ttu-id="6a77f-123">Nazwa docelowego serwera do przywrócenia.</span><span class="sxs-lookup"><span data-stu-id="6a77f-123">The dest server name to restore from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a77f-124">-Nowait</span><span class="sxs-lookup"><span data-stu-id="6a77f-124">-NoWait</span></span>
<span data-ttu-id="6a77f-125">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="6a77f-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6a77f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a77f-126">-ResourceGroupName</span></span>
<span data-ttu-id="6a77f-127">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="6a77f-127">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="6a77f-128">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="6a77f-128">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a77f-129">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="6a77f-129">-RestorePointInTime</span></span>
<span data-ttu-id="6a77f-130">Region PointInTimeRestore lokalizację, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="6a77f-130">region PointInTimeRestore The location the resource resides in.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a77f-131">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="6a77f-131">-ServerName</span></span>
<span data-ttu-id="6a77f-132">Nazwa serwera źródłowego do przywrócenia.</span><span class="sxs-lookup"><span data-stu-id="6a77f-132">The source server name to restore from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a77f-133">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="6a77f-133">-SubscriptionId</span></span>
<span data-ttu-id="6a77f-134">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6a77f-134">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="6a77f-135">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="6a77f-135">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a77f-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="6a77f-136">-Tag</span></span>
<span data-ttu-id="6a77f-137">Metadane specyficzne dla aplikacji w postaci par klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="6a77f-137">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="6a77f-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6a77f-138">-Confirm</span></span>
<span data-ttu-id="6a77f-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a77f-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a77f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a77f-140">-WhatIf</span></span>
<span data-ttu-id="6a77f-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a77f-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a77f-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6a77f-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a77f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a77f-143">CommonParameters</span></span>
<span data-ttu-id="6a77f-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a77f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a77f-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6a77f-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a77f-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6a77f-146">INPUTS</span></span>

### <span data-ttu-id="6a77f-147">Microsoft. Azure. PowerShell. polecenia. MariaDb. models. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="6a77f-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="6a77f-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6a77f-148">OUTPUTS</span></span>

### <span data-ttu-id="6a77f-149">Microsoft. Azure. PowerShell. polecenia. MariaDb. models. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="6a77f-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="6a77f-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6a77f-150">NOTES</span></span>

<span data-ttu-id="6a77f-151">PISUJE</span><span class="sxs-lookup"><span data-stu-id="6a77f-151">ALIASES</span></span>

<span data-ttu-id="6a77f-152">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6a77f-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6a77f-153">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="6a77f-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6a77f-154">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6a77f-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6a77f-155">WEJŚCIE <IServer> : obiekt serwera źródłowego do przywrócenia.</span><span class="sxs-lookup"><span data-stu-id="6a77f-155">INPUTOBJECT <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="6a77f-156">`Location <String>`: Lokalizacja, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="6a77f-156">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="6a77f-157">`[Tag <ITrackedResourceTags>]`: Metadane specyficzne dla aplikacji w postaci par klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="6a77f-157">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="6a77f-158">`[(Any) <String>]`: Wskazuje, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="6a77f-158">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="6a77f-159">`[AdministratorLogin <String>]`: Nazwa logowania administratora serwera.</span><span class="sxs-lookup"><span data-stu-id="6a77f-159">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="6a77f-160">Można określić tylko podczas tworzenia serwera (i jest on wymagany do utworzenia).</span><span class="sxs-lookup"><span data-stu-id="6a77f-160">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="6a77f-161">`[EarliestRestoreDate <DateTime?>]`: Najwcześniejszy czas tworzenia punktu przywracania (format ISO8601)</span><span class="sxs-lookup"><span data-stu-id="6a77f-161">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="6a77f-162">`[FullyQualifiedDomainName <String>]`: W pełni kwalifikowana nazwa domeny serwera.</span><span class="sxs-lookup"><span data-stu-id="6a77f-162">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="6a77f-163">`[IdentityType <IdentityType?>]`: Typ tożsamości.</span><span class="sxs-lookup"><span data-stu-id="6a77f-163">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="6a77f-164">Ustaw tę wartość na "SystemAssigned", aby automatycznie utworzyć i przypisać podmiot zabezpieczeń usługi Azure Active Directory dla tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="6a77f-164">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="6a77f-165">`[MasterServerId <String>]`: Identyfikator głównego serwera repliki.</span><span class="sxs-lookup"><span data-stu-id="6a77f-165">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="6a77f-166">`[ReplicaCapacity <Int32?>]`: Maksymalna liczba replik, które może mieć serwer główny.</span><span class="sxs-lookup"><span data-stu-id="6a77f-166">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="6a77f-167">`[ReplicationRole <String>]`: Rola replikacji serwera.</span><span class="sxs-lookup"><span data-stu-id="6a77f-167">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="6a77f-168">`[SkuCapacity <Int32?>]`: Wydajność skalowania w górę/poza, reprezentująca jednostki obliczeniowe serwera.</span><span class="sxs-lookup"><span data-stu-id="6a77f-168">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="6a77f-169">`[SkuFamily <String>]`: Rodzina sprzętu.</span><span class="sxs-lookup"><span data-stu-id="6a77f-169">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="6a77f-170">`[SkuName <String>]`: Nazwa jednostki SKU, zazwyczaj z rodziny + Rodzina + rdzenie, na przykład B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="6a77f-170">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="6a77f-171">`[SkuSize <String>]`: Kod rozmiaru, który ma być interpretowany według odpowiednich zasobów.</span><span class="sxs-lookup"><span data-stu-id="6a77f-171">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="6a77f-172">`[SkuTier <SkuTier?>]`: Warstwa konkretnej jednostki SKU, na przykład podstawowa.</span><span class="sxs-lookup"><span data-stu-id="6a77f-172">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="6a77f-173">`[SslEnforcement <SslEnforcementEnum?>]`: Włączanie wymuszania protokołu SSL lub nie podczas nawiązywania połączenia z serwerem.</span><span class="sxs-lookup"><span data-stu-id="6a77f-173">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="6a77f-174">`[StorageProfileBackupRetentionDay <Int32?>]`: Dni przechowywania kopii zapasowej serwera.</span><span class="sxs-lookup"><span data-stu-id="6a77f-174">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="6a77f-175">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Włączanie geograficznie nadmiarowych lub niezwiązanych z kopią zapasową serwera.</span><span class="sxs-lookup"><span data-stu-id="6a77f-175">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="6a77f-176">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Włączanie automatycznego zwiększania przestrzeni dyskowej.</span><span class="sxs-lookup"><span data-stu-id="6a77f-176">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="6a77f-177">`[StorageProfileStorageMb <Int32?>]`: Maksymalna ilość miejsca do magazynowania dozwolona dla serwera.</span><span class="sxs-lookup"><span data-stu-id="6a77f-177">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="6a77f-178">`[UserVisibleState <ServerState?>]`: Stan serwera, który jest widoczny dla użytkownika.</span><span class="sxs-lookup"><span data-stu-id="6a77f-178">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="6a77f-179">`[Version <ServerVersion?>]`: Wersja serwera.</span><span class="sxs-lookup"><span data-stu-id="6a77f-179">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="6a77f-180">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6a77f-180">RELATED LINKS</span></span>

