---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/new-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitorProviderInstance.md
ms.openlocfilehash: c9ba83218e8be82716f4804444b7c52371fe764c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98500959"
---
# <span data-ttu-id="83695-101">New-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="83695-101">New-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="83695-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="83695-102">SYNOPSIS</span></span>
<span data-ttu-id="83695-103">Tworzy wystąpienie dostawcy dla określonej subskrypcji, grupy zasobów, nazwy SapMonitor i nazwy zasobu.</span><span class="sxs-lookup"><span data-stu-id="83695-103">Creates a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="83695-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="83695-104">SYNTAX</span></span>

### <span data-ttu-id="83695-105">ByString (domyślny)</span><span class="sxs-lookup"><span data-stu-id="83695-105">ByString (Default)</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -HanaDatabaseName <String> -HanaDatabasePassword <SecureString> -HanaDatabaseSqlPort <Int32>
 -HanaDatabaseUsername <String> -HanaHostname <String> -ProviderType <String> [-SubscriptionId <String>]
 [-Metadata <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="83695-106">ByDict</span><span class="sxs-lookup"><span data-stu-id="83695-106">ByDict</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -InstanceProperty <Hashtable> -ProviderType <String> [-SubscriptionId <String>] [-Metadata <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="83695-107">ByKeyVault</span><span class="sxs-lookup"><span data-stu-id="83695-107">ByKeyVault</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -HanaDatabaseName <String> -HanaDatabasePasswordKeyVaultResourceId <String>
 -HanaDatabasePasswordSecretId <String> -HanaDatabaseSqlPort <Int32> -HanaDatabaseUsername <String>
 -HanaHostname <String> -ProviderType <String> [-SubscriptionId <String>] [-Metadata <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="83695-108">Opis</span><span class="sxs-lookup"><span data-stu-id="83695-108">DESCRIPTION</span></span>
<span data-ttu-id="83695-109">Tworzy wystąpienie dostawcy dla określonej subskrypcji, grupy zasobów, nazwy SapMonitor i nazwy zasobu.</span><span class="sxs-lookup"><span data-stu-id="83695-109">Creates a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="83695-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="83695-110">EXAMPLES</span></span>

### <span data-ttu-id="83695-111">Przykład 1. Tworzenie wystąpienia monitora protokołu SAP według ciągu dla HANA</span><span class="sxs-lookup"><span data-stu-id="83695-111">Example 1: Create an instance of SAP monitor by string for HANA</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -Name ps-sapmonitorins-t01 -SapMonitorName yemingmonitor -ProviderType SapHana -HanaHostname 'hdb1-0' -HanaDatabaseName 'SYSTEMDB' -HanaDatabaseSqlPort 30015 -HanaDatabaseUsername SYSTEM -HanaDatabasePassword (ConvertTo-SecureString "Manager1" -AsPlainText -Force)

Name                 Type
----                 ----
ps-sapmonitorins-t01 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="83695-112">To polecenie tworzy wystąpienie monitora protokołu SAP według ciągu dla obiektu HANA.</span><span class="sxs-lookup"><span data-stu-id="83695-112">This command creates an instance of SAP monitor by string for HANA.</span></span>

### <span data-ttu-id="83695-113">Przykład 2: Tworzenie wystąpienia monitora protokołu SAP według magazynu kluczy dla HANA</span><span class="sxs-lookup"><span data-stu-id="83695-113">Example 2: Create an instance of SAP monitor by key vault for HANA</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName sapMonitor-vayh7q-test -ProviderType SapHana -HanaHostname 'hdb1-0' -HanaDatabaseName 'SYSTEMDB' -HanaDatabaseSqlPort 30015 -HanaDatabaseUsername SYSTEM -HanaDatabasePasswordSecretId https://kv-9gosjc-test.vault.azure.net/secrets/hanaPassword/bf516d1dfcc144138e5cf55114f3344b -HanaDatabasePasswordKeyVaultResourceId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/costmanagement-rg-8p50xe/providers/Microsoft.KeyVault/vaults/kv-9gosjc-test -Name sapins-kv-test

Name           Type
----           ----
sapins-kv-test Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="83695-114">To polecenie tworzy wystąpienie monitora protokołu SAP według magazynu kluczy dla HANA.</span><span class="sxs-lookup"><span data-stu-id="83695-114">This command creates an instance of SAP monitor by key vault for HANA.</span></span>

### <span data-ttu-id="83695-115">Przykład 3: Tworzenie wystąpienia monitora protokołu SAP według słownika dla PrometheusHaCluster</span><span class="sxs-lookup"><span data-stu-id="83695-115">Example 3: Create an instance of SAP monitor by dictionary for PrometheusHaCluster</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-promclt   -SapMonitorName dolauli-test04 -ProviderType PrometheusHaCluster -InstanceProperty @{prometheusUrl='http://10.4.1.10:9664/metrics'}


Name                     Type
----                     ----
dolauli-instance-promclt Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="83695-116">To polecenie tworzy wystąpienie monitora protokołu SAP według słownika dla PrometheusHaCluster.</span><span class="sxs-lookup"><span data-stu-id="83695-116">This command creates an instance of SAP monitor by dictionary for PrometheusHaCluster.</span></span>

### <span data-ttu-id="83695-117">Przykład 4: Tworzenie wystąpienia monitora protokołu SAP według słownika dla PrometheusOS</span><span class="sxs-lookup"><span data-stu-id="83695-117">Example 4: Create an instance of SAP monitor by dictionary for PrometheusOS</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-prom   -SapMonitorName dolauli-test04 -ProviderType PrometheusOS -InstanceProperty @{prometheusUrl='http://10.3.1.6:9100/metrics'}

Name                  Type
----                  ----
dolauli-instance-prom Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="83695-118">To polecenie tworzy wystąpienie monitora protokołu SAP według słownika dla PrometheusOS.</span><span class="sxs-lookup"><span data-stu-id="83695-118">This command creates an instance of SAP monitor by dictionary for PrometheusOS.</span></span>

### <span data-ttu-id="83695-119">Przykład 5: Tworzenie wystąpienia monitora protokołu SAP według słownika dla MsSqlServer</span><span class="sxs-lookup"><span data-stu-id="83695-119">Example 5: Create an instance of SAP monitor by dictionary for MsSqlServer</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-ms   -SapMonitorName dolauli-test04 -ProviderType MsSqlServer -InstanceProperty @{sqlHostname="10.4.8.90";sqlPort=1433;sqlUsername="AMFSS";sqlPassword="fakepassword"}

Name                Type
----                ----
dolauli-instance-ms Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="83695-120">To polecenie tworzy wystąpienie monitora protokołu SAP według słownika dla MsSqlServer.</span><span class="sxs-lookup"><span data-stu-id="83695-120">This command creates an instance of SAP monitor by dictionary for MsSqlServer.</span></span>

### <span data-ttu-id="83695-121">Przykład 6: Tworzenie wystąpienia monitora protokołu SAP według słownika dla SapHana</span><span class="sxs-lookup"><span data-stu-id="83695-121">Example 6: Create an instance of SAP monitor by dictionary for SapHana</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-hana   -SapMonitorName dolauli-test04 -ProviderType SapHana -InstanceProperty @{hanaHostname="10.1.2.6";hanaDbName="SYSTEMDB";hanaDbSqlPort=30113;hanaDbUsername="SYSTEM"; hanaDbPassword="Manager1"}

Name                  Type
----                  ----
dolauli-instance-hana Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="83695-122">To polecenie tworzy wystąpienie monitora protokołu SAP według słownika dla SapHana.</span><span class="sxs-lookup"><span data-stu-id="83695-122">This command creates an instance of SAP monitor by dictionary for SapHana.</span></span>

## <span data-ttu-id="83695-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="83695-123">PARAMETERS</span></span>

### <span data-ttu-id="83695-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="83695-124">-AsJob</span></span>
<span data-ttu-id="83695-125">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="83695-125">Run the command as a job</span></span>

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

### <span data-ttu-id="83695-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83695-126">-DefaultProfile</span></span>
<span data-ttu-id="83695-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="83695-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83695-128">-HanaDatabaseName</span><span class="sxs-lookup"><span data-stu-id="83695-128">-HanaDatabaseName</span></span>
<span data-ttu-id="83695-129">Nazwa bazy danych wystąpienia SAP HANA.</span><span class="sxs-lookup"><span data-stu-id="83695-129">The database name of SAP HANA instance.</span></span>

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

### <span data-ttu-id="83695-130">-HanaDatabasePassword</span><span class="sxs-lookup"><span data-stu-id="83695-130">-HanaDatabasePassword</span></span>
<span data-ttu-id="83695-131">Hasło do bazy danych wystąpienia SAP HANA.</span><span class="sxs-lookup"><span data-stu-id="83695-131">The password of the database of SAP HANA instance.</span></span>

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

### <span data-ttu-id="83695-132">-HanaDatabasePasswordKeyVaultResourceId</span><span class="sxs-lookup"><span data-stu-id="83695-132">-HanaDatabasePasswordKeyVaultResourceId</span></span>
<span data-ttu-id="83695-133">Identyfikator zasobu magazynu kluczy zawierającego poświadczenia HANA.</span><span class="sxs-lookup"><span data-stu-id="83695-133">Resource ID of the Key Vault that contains the HANA credentials.</span></span>

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

### <span data-ttu-id="83695-134">-HanaDatabasePasswordSecretId</span><span class="sxs-lookup"><span data-stu-id="83695-134">-HanaDatabasePasswordSecretId</span></span>
<span data-ttu-id="83695-135">Tajny identyfikator tajnego magazynu kluczy, który zawiera poświadczenia HANA.</span><span class="sxs-lookup"><span data-stu-id="83695-135">Secret identifier to the Key Vault secret that contains the HANA credentials.</span></span>

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

### <span data-ttu-id="83695-136">-HanaDatabaseSqlPort</span><span class="sxs-lookup"><span data-stu-id="83695-136">-HanaDatabaseSqlPort</span></span>
<span data-ttu-id="83695-137">Port SQL bazy danych wystąpienia SAP HANA.</span><span class="sxs-lookup"><span data-stu-id="83695-137">The SQL port of the database of SAP HANA instance.</span></span>

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

### <span data-ttu-id="83695-138">-HanaDatabaseUsername</span><span class="sxs-lookup"><span data-stu-id="83695-138">-HanaDatabaseUsername</span></span>
<span data-ttu-id="83695-139">Nazwa użytkownika bazy danych wystąpienia SAP HANA.</span><span class="sxs-lookup"><span data-stu-id="83695-139">The username of the database of SAP HANA instance.</span></span>

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

### <span data-ttu-id="83695-140">-HanaHostname</span><span class="sxs-lookup"><span data-stu-id="83695-140">-HanaHostname</span></span>
<span data-ttu-id="83695-141">Nazwa hosta wystąpienia SAP HANA.</span><span class="sxs-lookup"><span data-stu-id="83695-141">The hostname of SAP HANA instance.</span></span>

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

### <span data-ttu-id="83695-142">-InstanceProperty</span><span class="sxs-lookup"><span data-stu-id="83695-142">-InstanceProperty</span></span>
<span data-ttu-id="83695-143">Właściwość wystąpienia usługi HANA.</span><span class="sxs-lookup"><span data-stu-id="83695-143">The property of HANA instance.</span></span>

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

### <span data-ttu-id="83695-144">-Metadata</span><span class="sxs-lookup"><span data-stu-id="83695-144">-Metadata</span></span>
<span data-ttu-id="83695-145">Ciąg JSON zawierający metadane wystąpienia dostawcy.</span><span class="sxs-lookup"><span data-stu-id="83695-145">A JSON string containing metadata of the provider instance.</span></span>

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

### <span data-ttu-id="83695-146">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="83695-146">-Name</span></span>
<span data-ttu-id="83695-147">Nazwa wystąpienia dostawcy.</span><span class="sxs-lookup"><span data-stu-id="83695-147">Name of the provider instance.</span></span>

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

### <span data-ttu-id="83695-148">-Nowait</span><span class="sxs-lookup"><span data-stu-id="83695-148">-NoWait</span></span>
<span data-ttu-id="83695-149">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="83695-149">Run the command asynchronously</span></span>

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

### <span data-ttu-id="83695-150">-ProviderType</span><span class="sxs-lookup"><span data-stu-id="83695-150">-ProviderType</span></span>
<span data-ttu-id="83695-151">Typ wystąpienia dostawcy.</span><span class="sxs-lookup"><span data-stu-id="83695-151">The type of provider instance.</span></span>
<span data-ttu-id="83695-152">Obsługiwane wartości to: "SapHana".</span><span class="sxs-lookup"><span data-stu-id="83695-152">Supported values are: "SapHana".</span></span>

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

### <span data-ttu-id="83695-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83695-153">-ResourceGroupName</span></span>
<span data-ttu-id="83695-154">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="83695-154">Name of the resource group.</span></span>

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

### <span data-ttu-id="83695-155">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="83695-155">-SapMonitorName</span></span>
<span data-ttu-id="83695-156">Nazwa zasobu monitorowania protokołu SAP.</span><span class="sxs-lookup"><span data-stu-id="83695-156">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="83695-157">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="83695-157">-SubscriptionId</span></span>
<span data-ttu-id="83695-158">Identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="83695-158">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="83695-159">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="83695-159">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="83695-160">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="83695-160">-Confirm</span></span>
<span data-ttu-id="83695-161">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83695-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83695-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83695-162">-WhatIf</span></span>
<span data-ttu-id="83695-163">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83695-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83695-164">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="83695-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83695-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83695-165">CommonParameters</span></span>
<span data-ttu-id="83695-166">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83695-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83695-167">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="83695-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83695-168">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="83695-168">INPUTS</span></span>

## <span data-ttu-id="83695-169">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="83695-169">OUTPUTS</span></span>

### <span data-ttu-id="83695-170">Microsoft. Azure. PowerShell. polecenia. HanaOnAzure. models. Api20200207Preview. IProviderInstance</span><span class="sxs-lookup"><span data-stu-id="83695-170">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span></span>

## <span data-ttu-id="83695-171">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="83695-171">NOTES</span></span>

<span data-ttu-id="83695-172">PISUJE</span><span class="sxs-lookup"><span data-stu-id="83695-172">ALIASES</span></span>

## <span data-ttu-id="83695-173">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="83695-173">RELATED LINKS</span></span>

