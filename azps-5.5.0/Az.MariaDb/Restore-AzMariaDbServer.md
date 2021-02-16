---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/restore-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restore-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restore-AzMariaDbServer.md
ms.openlocfilehash: 95988d83cbb4c3dcf0b5da890bf38f8c40eb4dfa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241243"
---
# <span data-ttu-id="8e1bf-101">Restore-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="8e1bf-101">Restore-AzMariaDbServer</span></span>

## <span data-ttu-id="8e1bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e1bf-102">SYNOPSIS</span></span>
<span data-ttu-id="8e1bf-103">Przywracanie bazy danych MariaDB z istniejącej bazy danych MariaDB.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-103">Restore a MariaDB from a existing MariaDB.</span></span>

## <span data-ttu-id="8e1bf-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8e1bf-104">SYNTAX</span></span>

```
Restore-AzMariaDbServer -Name <String> -RestorePointInTime <DateTime> [-InputObject <IServer>]
 [-ResourceGroupName <String>] [-ServerName <String>] [-SubscriptionId <String>] [-Location <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8e1bf-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8e1bf-105">DESCRIPTION</span></span>
<span data-ttu-id="8e1bf-106">Przywracanie bazy danych MariaDB z istniejącej bazy danych MariaDB.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-106">Restore a MariaDB from a existing MariaDB.</span></span>

## <span data-ttu-id="8e1bf-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8e1bf-107">EXAMPLES</span></span>

### <span data-ttu-id="8e1bf-108">Przykład 1. Przywracanie pliku PointInTime MariaDB według nazwy serwera.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-108">Example 1: Restore a PointInTime MariaDB by server name.</span></span>
```powershell
PS C:\> Restore-AzMariaDbServer -Name restore-db01 -ServerName mariadb-test-usegeo -ResourceGroupName mariadb-test-4rih5z -UsePointInTimeRestore -RestorePointInTime $(Get-Date) -Location eastus

Name         Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----         -------- ------------------ ------- ----------------------- -------   -------        --------------
restore-db01 eastus   adminuser          10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="8e1bf-109">To polecenie pozwala przywrócić plik PointInTime MariaDB według nazwy serwera.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-109">This command restore a PointInTime MariaDB by server name.</span></span>

### <span data-ttu-id="8e1bf-110">Przykład 2. Przywracanie obiektu PointInTime MariaDB według obiektu serwera</span><span class="sxs-lookup"><span data-stu-id="8e1bf-110">Example 2: Restore a PointInTime MariaDB by server object</span></span>
```powershell
PS C:\> $db = Get-AzMariaDbServer -Name mariadb-test-usegeo -ResourceGroupName mariadb-test-4rih5z
PS C:\>Restore-AzMariaDbServer -Name restore-db02 -InputObject $db -UsePointInTimeRestore -RestorePointInTime $(Get-Date) -Location eastus

Name         Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----         -------- ------------------ ------- ----------------------- -------   -------        --------------
restore-db02 eastus   adminuser          10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="8e1bf-111">To polecenie pozwala przywrócić obiekt PointInTime MariaDB według obiektu serwera.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-111">This command restore a PointInTime MariaDB by server object.</span></span>

## <span data-ttu-id="8e1bf-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e1bf-112">PARAMETERS</span></span>

### <span data-ttu-id="8e1bf-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="8e1bf-113">-AsJob</span></span>
<span data-ttu-id="8e1bf-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="8e1bf-114">Run the command as a job</span></span>

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

### <span data-ttu-id="8e1bf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e1bf-115">-DefaultProfile</span></span>
<span data-ttu-id="8e1bf-116">Region DefaultParameters Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-116">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e1bf-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e1bf-117">-InputObject</span></span>
<span data-ttu-id="8e1bf-118">Obiekt serwera źródłowego, z którym chcesz przywrócić dane.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-118">The source server object to restore from.</span></span>
<span data-ttu-id="8e1bf-119">Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach inputOBJECT i utworzyć tabelę skrótów.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-119">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8e1bf-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="8e1bf-120">-Location</span></span>
<span data-ttu-id="8e1bf-121">Lokalizacja, w którym znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-121">The location the resource resides in.</span></span>

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

### <span data-ttu-id="8e1bf-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8e1bf-122">-Name</span></span>
<span data-ttu-id="8e1bf-123">Nazwa serwera dest, z którym chcesz przywrócić dane.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-123">The dest server name to restore from.</span></span>

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

### <span data-ttu-id="8e1bf-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8e1bf-124">-NoWait</span></span>
<span data-ttu-id="8e1bf-125">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="8e1bf-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8e1bf-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e1bf-126">-ResourceGroupName</span></span>
<span data-ttu-id="8e1bf-127">Nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-127">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="8e1bf-128">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-128">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="8e1bf-129">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="8e1bf-129">-RestorePointInTime</span></span>
<span data-ttu-id="8e1bf-130">region PointInTimeRestore Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-130">region PointInTimeRestore The location the resource resides in.</span></span>

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

### <span data-ttu-id="8e1bf-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8e1bf-131">-ServerName</span></span>
<span data-ttu-id="8e1bf-132">Nazwa serwera źródłowego, z którym chcesz przywrócić dane.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-132">The source server name to restore from.</span></span>

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

### <span data-ttu-id="8e1bf-133">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8e1bf-133">-SubscriptionId</span></span>
<span data-ttu-id="8e1bf-134">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-134">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="8e1bf-135">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-135">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8e1bf-136">— Tag</span><span class="sxs-lookup"><span data-stu-id="8e1bf-136">-Tag</span></span>
<span data-ttu-id="8e1bf-137">Metadane specyficzne dla aplikacji w postaci par klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-137">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="8e1bf-138">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8e1bf-138">-Confirm</span></span>
<span data-ttu-id="8e1bf-139">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e1bf-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e1bf-140">-WhatIf</span></span>
<span data-ttu-id="8e1bf-141">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e1bf-142">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e1bf-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e1bf-143">CommonParameters</span></span>
<span data-ttu-id="8e1bf-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e1bf-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e1bf-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e1bf-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8e1bf-146">INPUTS</span></span>

### <span data-ttu-id="8e1bf-147">Microsoft.Azure.PowerShell.cmdlet.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="8e1bf-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="8e1bf-148">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8e1bf-148">OUTPUTS</span></span>

### <span data-ttu-id="8e1bf-149">Microsoft.Azure.PowerShell.cmdlet.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="8e1bf-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="8e1bf-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8e1bf-150">NOTES</span></span>

<span data-ttu-id="8e1bf-151">ALIASY</span><span class="sxs-lookup"><span data-stu-id="8e1bf-151">ALIASES</span></span>

<span data-ttu-id="8e1bf-152">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8e1bf-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8e1bf-153">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8e1bf-154">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8e1bf-155">INPUTOBJECT: <IServer> obiekt serwera źródłowego, z którym należy przywrócić dane.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-155">INPUTOBJECT <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="8e1bf-156">`Location <String>`: lokalizacja, w którym znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-156">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="8e1bf-157">`[Tag <ITrackedResourceTags>]`: Metadane specyficzne dla aplikacji w postaci par klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-157">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="8e1bf-158">`[(Any) <String>]`: Wskazuje to, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-158">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="8e1bf-159">`[AdministratorLogin <String>]`: nazwa logowania administratora serwera.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-159">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="8e1bf-160">Można określić tylko wtedy, gdy serwer jest tworzony (i jest wymagany do utworzenia).</span><span class="sxs-lookup"><span data-stu-id="8e1bf-160">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="8e1bf-161">`[EarliestRestoreDate <DateTime?>]`: najwcześniejszy czas tworzenia punktów przywracania (format ISO8601)</span><span class="sxs-lookup"><span data-stu-id="8e1bf-161">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="8e1bf-162">`[FullyQualifiedDomainName <String>]`: w pełni kwalifikowana nazwa domeny serwera.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-162">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="8e1bf-163">`[IdentityType <IdentityType?>]`: typ tożsamości.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-163">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="8e1bf-164">Ustaw tę wartość na "SystemAssigned", aby automatycznie utworzyć i przypisać do zasobu podmiot zabezpieczeń usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-164">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="8e1bf-165">`[MasterServerId <String>]`: Główny identyfikator serwera repliki.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-165">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="8e1bf-166">`[ReplicaCapacity <Int32?>]`: Maksymalna liczba replik, które może mieć serwer główny.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-166">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="8e1bf-167">`[ReplicationRole <String>]`: rola replikacji serwera.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-167">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="8e1bf-168">`[SkuCapacity <Int32?>]`: Skalowanie wydajności w górę/wy, czyli jednostek obliczeniowych serwera.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-168">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="8e1bf-169">`[SkuFamily <String>]`: Rodzina sprzętu.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-169">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="8e1bf-170">`[SkuName <String>]`: nazwa sKU, zazwyczaj warstwa + rodzina + core, na przykład B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-170">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="8e1bf-171">`[SkuSize <String>]`: Kod rozmiaru, który ma być interpretowany przez zasób w zależności od potrzeb.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-171">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="8e1bf-172">`[SkuTier <SkuTier?>]`: warstwa określonej wersji SKU, np. Podstawowa.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-172">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="8e1bf-173">`[SslEnforcement <SslEnforcementEnum?>]`: Włącz wymuszanie ssl lub nie wymusz w przypadku łączenia się z serwerem.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-173">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="8e1bf-174">`[StorageProfileBackupRetentionDay <Int32?>]`: Dni przechowywania kopii zapasowej dla serwera.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-174">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="8e1bf-175">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Włącz funkcję nadmiarowej lokalizacji geograficznej lub nie umożliwia tworzenia kopii zapasowej na serwerze.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-175">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="8e1bf-176">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Włącz automatyczne powiększanie magazynu.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-176">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="8e1bf-177">`[StorageProfileStorageMb <Int32?>]`: Maksymalna dozwolona przestrzeń dyskowa na serwerze.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-177">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="8e1bf-178">`[UserVisibleState <ServerState?>]`: stan serwera, który jest widoczny dla użytkownika.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-178">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="8e1bf-179">`[Version <ServerVersion?>]`: Wersja serwera.</span><span class="sxs-lookup"><span data-stu-id="8e1bf-179">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="8e1bf-180">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8e1bf-180">RELATED LINKS</span></span>

