---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/new-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitorProviderInstance.md
ms.openlocfilehash: c9ba83218e8be82716f4804444b7c52371fe764c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185827"
---
# <span data-ttu-id="345aa-101">New-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="345aa-101">New-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="345aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="345aa-102">SYNOPSIS</span></span>
<span data-ttu-id="345aa-103">Tworzy wystąpienie dostawcy dla określonej subskrypcji, grupy zasobów, nazwy SapMonitor i nazwy zasobu.</span><span class="sxs-lookup"><span data-stu-id="345aa-103">Creates a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="345aa-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="345aa-104">SYNTAX</span></span>

### <span data-ttu-id="345aa-105">ByString (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="345aa-105">ByString (Default)</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -HanaDatabaseName <String> -HanaDatabasePassword <SecureString> -HanaDatabaseSqlPort <Int32>
 -HanaDatabaseUsername <String> -HanaHostname <String> -ProviderType <String> [-SubscriptionId <String>]
 [-Metadata <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="345aa-106">ByDict</span><span class="sxs-lookup"><span data-stu-id="345aa-106">ByDict</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -InstanceProperty <Hashtable> -ProviderType <String> [-SubscriptionId <String>] [-Metadata <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="345aa-107">ByKeyVault</span><span class="sxs-lookup"><span data-stu-id="345aa-107">ByKeyVault</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -HanaDatabaseName <String> -HanaDatabasePasswordKeyVaultResourceId <String>
 -HanaDatabasePasswordSecretId <String> -HanaDatabaseSqlPort <Int32> -HanaDatabaseUsername <String>
 -HanaHostname <String> -ProviderType <String> [-SubscriptionId <String>] [-Metadata <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="345aa-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="345aa-108">DESCRIPTION</span></span>
<span data-ttu-id="345aa-109">Tworzy wystąpienie dostawcy dla określonej subskrypcji, grupy zasobów, nazwy SapMonitor i nazwy zasobu.</span><span class="sxs-lookup"><span data-stu-id="345aa-109">Creates a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="345aa-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="345aa-110">EXAMPLES</span></span>

### <span data-ttu-id="345aa-111">Przykład 1. Tworzenie wystąpienia monitora SAP według ciągów dla usługi HANA</span><span class="sxs-lookup"><span data-stu-id="345aa-111">Example 1: Create an instance of SAP monitor by string for HANA</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -Name ps-sapmonitorins-t01 -SapMonitorName yemingmonitor -ProviderType SapHana -HanaHostname 'hdb1-0' -HanaDatabaseName 'SYSTEMDB' -HanaDatabaseSqlPort 30015 -HanaDatabaseUsername SYSTEM -HanaDatabasePassword (ConvertTo-SecureString "Manager1" -AsPlainText -Force)

Name                 Type
----                 ----
ps-sapmonitorins-t01 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="345aa-112">To polecenie tworzy wystąpienie monitora SAP według ciągu dla usługi HANA.</span><span class="sxs-lookup"><span data-stu-id="345aa-112">This command creates an instance of SAP monitor by string for HANA.</span></span>

### <span data-ttu-id="345aa-113">Przykład 2. Tworzenie wystąpienia monitora SAP według magazynu kluczy dla usługi HANA</span><span class="sxs-lookup"><span data-stu-id="345aa-113">Example 2: Create an instance of SAP monitor by key vault for HANA</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName sapMonitor-vayh7q-test -ProviderType SapHana -HanaHostname 'hdb1-0' -HanaDatabaseName 'SYSTEMDB' -HanaDatabaseSqlPort 30015 -HanaDatabaseUsername SYSTEM -HanaDatabasePasswordSecretId https://kv-9gosjc-test.vault.azure.net/secrets/hanaPassword/bf516d1dfcc144138e5cf55114f3344b -HanaDatabasePasswordKeyVaultResourceId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/costmanagement-rg-8p50xe/providers/Microsoft.KeyVault/vaults/kv-9gosjc-test -Name sapins-kv-test

Name           Type
----           ----
sapins-kv-test Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="345aa-114">To polecenie tworzy wystąpienie monitora SAP według magazynu kluczy dla usługi HANA.</span><span class="sxs-lookup"><span data-stu-id="345aa-114">This command creates an instance of SAP monitor by key vault for HANA.</span></span>

### <span data-ttu-id="345aa-115">Przykład 3. Tworzenie wystąpienia monitora SAP według słownika dla aplikacji PrometheusHaCluster</span><span class="sxs-lookup"><span data-stu-id="345aa-115">Example 3: Create an instance of SAP monitor by dictionary for PrometheusHaCluster</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-promclt   -SapMonitorName dolauli-test04 -ProviderType PrometheusHaCluster -InstanceProperty @{prometheusUrl='http://10.4.1.10:9664/metrics'}


Name                     Type
----                     ----
dolauli-instance-promclt Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="345aa-116">To polecenie tworzy wystąpienie monitora SAP według słownika dla użytkownika PrometheusHaCluster.</span><span class="sxs-lookup"><span data-stu-id="345aa-116">This command creates an instance of SAP monitor by dictionary for PrometheusHaCluster.</span></span>

### <span data-ttu-id="345aa-117">Przykład 4. Tworzenie wystąpienia monitora SAP według słownika dla aplikacji PrometheusOS</span><span class="sxs-lookup"><span data-stu-id="345aa-117">Example 4: Create an instance of SAP monitor by dictionary for PrometheusOS</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-prom   -SapMonitorName dolauli-test04 -ProviderType PrometheusOS -InstanceProperty @{prometheusUrl='http://10.3.1.6:9100/metrics'}

Name                  Type
----                  ----
dolauli-instance-prom Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="345aa-118">To polecenie tworzy wystąpienie monitora SAP według słownika dla aplikacji PrometheusOS.</span><span class="sxs-lookup"><span data-stu-id="345aa-118">This command creates an instance of SAP monitor by dictionary for PrometheusOS.</span></span>

### <span data-ttu-id="345aa-119">Przykład 5. Tworzenie wystąpienia monitora SAP według słownika dla serwera MsSqlServer</span><span class="sxs-lookup"><span data-stu-id="345aa-119">Example 5: Create an instance of SAP monitor by dictionary for MsSqlServer</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-ms   -SapMonitorName dolauli-test04 -ProviderType MsSqlServer -InstanceProperty @{sqlHostname="10.4.8.90";sqlPort=1433;sqlUsername="AMFSS";sqlPassword="fakepassword"}

Name                Type
----                ----
dolauli-instance-ms Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="345aa-120">To polecenie tworzy wystąpienie monitora SAP według słownika dla serwera MsSqlServer.</span><span class="sxs-lookup"><span data-stu-id="345aa-120">This command creates an instance of SAP monitor by dictionary for MsSqlServer.</span></span>

### <span data-ttu-id="345aa-121">Przykład 6. Tworzenie wystąpienia monitora SAP według słownika dla aplikacji SapHana</span><span class="sxs-lookup"><span data-stu-id="345aa-121">Example 6: Create an instance of SAP monitor by dictionary for SapHana</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-hana   -SapMonitorName dolauli-test04 -ProviderType SapHana -InstanceProperty @{hanaHostname="10.1.2.6";hanaDbName="SYSTEMDB";hanaDbSqlPort=30113;hanaDbUsername="SYSTEM"; hanaDbPassword="Manager1"}

Name                  Type
----                  ----
dolauli-instance-hana Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="345aa-122">To polecenie tworzy wystąpienie monitora SAP według słownika dla aplikacji SapHana.</span><span class="sxs-lookup"><span data-stu-id="345aa-122">This command creates an instance of SAP monitor by dictionary for SapHana.</span></span>

## <span data-ttu-id="345aa-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="345aa-123">PARAMETERS</span></span>

### <span data-ttu-id="345aa-124">— AsJob</span><span class="sxs-lookup"><span data-stu-id="345aa-124">-AsJob</span></span>
<span data-ttu-id="345aa-125">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="345aa-125">Run the command as a job</span></span>

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

### <span data-ttu-id="345aa-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="345aa-126">-DefaultProfile</span></span>
<span data-ttu-id="345aa-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="345aa-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="345aa-128">-HanaDatabaseName</span><span class="sxs-lookup"><span data-stu-id="345aa-128">-HanaDatabaseName</span></span>
<span data-ttu-id="345aa-129">Nazwa bazy danych wystąpienia sap HANA.</span><span class="sxs-lookup"><span data-stu-id="345aa-129">The database name of SAP HANA instance.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyVault, ByString
Aliases: HanaDbName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="345aa-130">-HanaDatabasePassword</span><span class="sxs-lookup"><span data-stu-id="345aa-130">-HanaDatabasePassword</span></span>
<span data-ttu-id="345aa-131">Hasło bazy danych wystąpienia sap HANA.</span><span class="sxs-lookup"><span data-stu-id="345aa-131">The password of the database of SAP HANA instance.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByString
Aliases: HanaDbPassword

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="345aa-132">-HanaDatabasePasswordKeyVaultResourceId</span><span class="sxs-lookup"><span data-stu-id="345aa-132">-HanaDatabasePasswordKeyVaultResourceId</span></span>
<span data-ttu-id="345aa-133">Identyfikator zasobu magazynu kluczy zawierający poświadczenia HANA.</span><span class="sxs-lookup"><span data-stu-id="345aa-133">Resource ID of the Key Vault that contains the HANA credentials.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyVault
Aliases: HanaDbPasswordKeyVaultId, KeyVaultId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="345aa-134">-HanaDatabasePasswordSecretId</span><span class="sxs-lookup"><span data-stu-id="345aa-134">-HanaDatabasePasswordSecretId</span></span>
<span data-ttu-id="345aa-135">Tajny identyfikator magazynu kluczy zawierający poświadczenia HANA.</span><span class="sxs-lookup"><span data-stu-id="345aa-135">Secret identifier to the Key Vault secret that contains the HANA credentials.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyVault
Aliases: HanaDbPasswordSecretId, SecretId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="345aa-136">-HanaDatabaseSqlPort</span><span class="sxs-lookup"><span data-stu-id="345aa-136">-HanaDatabaseSqlPort</span></span>
<span data-ttu-id="345aa-137">Port SQL bazy danych wystąpienia sap HANA.</span><span class="sxs-lookup"><span data-stu-id="345aa-137">The SQL port of the database of SAP HANA instance.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByKeyVault, ByString
Aliases: HanaDbSqlPort

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="345aa-138">-HanaDatabaseUsername</span><span class="sxs-lookup"><span data-stu-id="345aa-138">-HanaDatabaseUsername</span></span>
<span data-ttu-id="345aa-139">Nazwa użytkownika bazy danych wystąpienia usługi SAP HANA.</span><span class="sxs-lookup"><span data-stu-id="345aa-139">The username of the database of SAP HANA instance.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyVault, ByString
Aliases: HanaDbUsername

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="345aa-140">-HanaHostname</span><span class="sxs-lookup"><span data-stu-id="345aa-140">-HanaHostname</span></span>
<span data-ttu-id="345aa-141">Nazwa hosta wystąpienia sap HANA.</span><span class="sxs-lookup"><span data-stu-id="345aa-141">The hostname of SAP HANA instance.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyVault, ByString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="345aa-142">-InstanceProperty</span><span class="sxs-lookup"><span data-stu-id="345aa-142">-InstanceProperty</span></span>
<span data-ttu-id="345aa-143">Właściwość wystąpienia hana.</span><span class="sxs-lookup"><span data-stu-id="345aa-143">The property of HANA instance.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByDict
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="345aa-144">— Metadane</span><span class="sxs-lookup"><span data-stu-id="345aa-144">-Metadata</span></span>
<span data-ttu-id="345aa-145">Ciąg JSON zawierający metadane wystąpienia dostawcy.</span><span class="sxs-lookup"><span data-stu-id="345aa-145">A JSON string containing metadata of the provider instance.</span></span>

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

### <span data-ttu-id="345aa-146">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="345aa-146">-Name</span></span>
<span data-ttu-id="345aa-147">Nazwa wystąpienia dostawcy.</span><span class="sxs-lookup"><span data-stu-id="345aa-147">Name of the provider instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProviderInstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="345aa-148">-NoWait</span><span class="sxs-lookup"><span data-stu-id="345aa-148">-NoWait</span></span>
<span data-ttu-id="345aa-149">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="345aa-149">Run the command asynchronously</span></span>

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

### <span data-ttu-id="345aa-150">-ProviderType</span><span class="sxs-lookup"><span data-stu-id="345aa-150">-ProviderType</span></span>
<span data-ttu-id="345aa-151">Typ wystąpienia dostawcy.</span><span class="sxs-lookup"><span data-stu-id="345aa-151">The type of provider instance.</span></span>
<span data-ttu-id="345aa-152">Obsługiwane wartości to: "SapHana".</span><span class="sxs-lookup"><span data-stu-id="345aa-152">Supported values are: "SapHana".</span></span>

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

### <span data-ttu-id="345aa-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="345aa-153">-ResourceGroupName</span></span>
<span data-ttu-id="345aa-154">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="345aa-154">Name of the resource group.</span></span>

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

### <span data-ttu-id="345aa-155">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="345aa-155">-SapMonitorName</span></span>
<span data-ttu-id="345aa-156">Nazwa zasobu monitorowego SAP.</span><span class="sxs-lookup"><span data-stu-id="345aa-156">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="345aa-157">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="345aa-157">-SubscriptionId</span></span>
<span data-ttu-id="345aa-158">Identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="345aa-158">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="345aa-159">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="345aa-159">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="345aa-160">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="345aa-160">-Confirm</span></span>
<span data-ttu-id="345aa-161">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="345aa-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="345aa-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="345aa-162">-WhatIf</span></span>
<span data-ttu-id="345aa-163">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="345aa-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="345aa-164">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="345aa-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="345aa-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="345aa-165">CommonParameters</span></span>
<span data-ttu-id="345aa-166">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="345aa-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="345aa-167">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="345aa-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="345aa-168">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="345aa-168">INPUTS</span></span>

## <span data-ttu-id="345aa-169">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="345aa-169">OUTPUTS</span></span>

### <span data-ttu-id="345aa-170">Microsoft.Azure.PowerShell.Cmdlet.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span><span class="sxs-lookup"><span data-stu-id="345aa-170">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span></span>

## <span data-ttu-id="345aa-171">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="345aa-171">NOTES</span></span>

<span data-ttu-id="345aa-172">ALIASY</span><span class="sxs-lookup"><span data-stu-id="345aa-172">ALIASES</span></span>

## <span data-ttu-id="345aa-173">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="345aa-173">RELATED LINKS</span></span>

