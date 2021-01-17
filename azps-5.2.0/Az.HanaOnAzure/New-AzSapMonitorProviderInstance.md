---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/new-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitorProviderInstance.md
ms.openlocfilehash: c9ba83218e8be82716f4804444b7c52371fe764c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332206"
---
# <span data-ttu-id="259da-101">New-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="259da-101">New-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="259da-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="259da-102">SYNOPSIS</span></span>
<span data-ttu-id="259da-103">Tworzy wystąpienie dostawcy dla określonej subskrypcji, grupy zasobów, nazwy SapMonitor i nazwy zasobu.</span><span class="sxs-lookup"><span data-stu-id="259da-103">Creates a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="259da-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="259da-104">SYNTAX</span></span>

### <span data-ttu-id="259da-105">ByString (domyślny)</span><span class="sxs-lookup"><span data-stu-id="259da-105">ByString (Default)</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -HanaDatabaseName <String> -HanaDatabasePassword <SecureString> -HanaDatabaseSqlPort <Int32>
 -HanaDatabaseUsername <String> -HanaHostname <String> -ProviderType <String> [-SubscriptionId <String>]
 [-Metadata <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="259da-106">ByDict</span><span class="sxs-lookup"><span data-stu-id="259da-106">ByDict</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -InstanceProperty <Hashtable> -ProviderType <String> [-SubscriptionId <String>] [-Metadata <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="259da-107">ByKeyVault</span><span class="sxs-lookup"><span data-stu-id="259da-107">ByKeyVault</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -HanaDatabaseName <String> -HanaDatabasePasswordKeyVaultResourceId <String>
 -HanaDatabasePasswordSecretId <String> -HanaDatabaseSqlPort <Int32> -HanaDatabaseUsername <String>
 -HanaHostname <String> -ProviderType <String> [-SubscriptionId <String>] [-Metadata <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="259da-108">Opis</span><span class="sxs-lookup"><span data-stu-id="259da-108">DESCRIPTION</span></span>
<span data-ttu-id="259da-109">Tworzy wystąpienie dostawcy dla określonej subskrypcji, grupy zasobów, nazwy SapMonitor i nazwy zasobu.</span><span class="sxs-lookup"><span data-stu-id="259da-109">Creates a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="259da-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="259da-110">EXAMPLES</span></span>

### <span data-ttu-id="259da-111">Przykład 1. Tworzenie wystąpienia monitora protokołu SAP według ciągu dla HANA</span><span class="sxs-lookup"><span data-stu-id="259da-111">Example 1: Create an instance of SAP monitor by string for HANA</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -Name ps-sapmonitorins-t01 -SapMonitorName yemingmonitor -ProviderType SapHana -HanaHostname 'hdb1-0' -HanaDatabaseName 'SYSTEMDB' -HanaDatabaseSqlPort 30015 -HanaDatabaseUsername SYSTEM -HanaDatabasePassword (ConvertTo-SecureString "Manager1" -AsPlainText -Force)

Name                 Type
----                 ----
ps-sapmonitorins-t01 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="259da-112">To polecenie tworzy wystąpienie monitora protokołu SAP według ciągu dla obiektu HANA.</span><span class="sxs-lookup"><span data-stu-id="259da-112">This command creates an instance of SAP monitor by string for HANA.</span></span>

### <span data-ttu-id="259da-113">Przykład 2: Tworzenie wystąpienia monitora protokołu SAP według magazynu kluczy dla HANA</span><span class="sxs-lookup"><span data-stu-id="259da-113">Example 2: Create an instance of SAP monitor by key vault for HANA</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName sapMonitor-vayh7q-test -ProviderType SapHana -HanaHostname 'hdb1-0' -HanaDatabaseName 'SYSTEMDB' -HanaDatabaseSqlPort 30015 -HanaDatabaseUsername SYSTEM -HanaDatabasePasswordSecretId https://kv-9gosjc-test.vault.azure.net/secrets/hanaPassword/bf516d1dfcc144138e5cf55114f3344b -HanaDatabasePasswordKeyVaultResourceId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/costmanagement-rg-8p50xe/providers/Microsoft.KeyVault/vaults/kv-9gosjc-test -Name sapins-kv-test

Name           Type
----           ----
sapins-kv-test Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="259da-114">To polecenie tworzy wystąpienie monitora protokołu SAP według magazynu kluczy dla HANA.</span><span class="sxs-lookup"><span data-stu-id="259da-114">This command creates an instance of SAP monitor by key vault for HANA.</span></span>

### <span data-ttu-id="259da-115">Przykład 3: Tworzenie wystąpienia monitora protokołu SAP według słownika dla PrometheusHaCluster</span><span class="sxs-lookup"><span data-stu-id="259da-115">Example 3: Create an instance of SAP monitor by dictionary for PrometheusHaCluster</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-promclt   -SapMonitorName dolauli-test04 -ProviderType PrometheusHaCluster -InstanceProperty @{prometheusUrl='http://10.4.1.10:9664/metrics'}


Name                     Type
----                     ----
dolauli-instance-promclt Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="259da-116">To polecenie tworzy wystąpienie monitora protokołu SAP według słownika dla PrometheusHaCluster.</span><span class="sxs-lookup"><span data-stu-id="259da-116">This command creates an instance of SAP monitor by dictionary for PrometheusHaCluster.</span></span>

### <span data-ttu-id="259da-117">Przykład 4: Tworzenie wystąpienia monitora protokołu SAP według słownika dla PrometheusOS</span><span class="sxs-lookup"><span data-stu-id="259da-117">Example 4: Create an instance of SAP monitor by dictionary for PrometheusOS</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-prom   -SapMonitorName dolauli-test04 -ProviderType PrometheusOS -InstanceProperty @{prometheusUrl='http://10.3.1.6:9100/metrics'}

Name                  Type
----                  ----
dolauli-instance-prom Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="259da-118">To polecenie tworzy wystąpienie monitora protokołu SAP według słownika dla PrometheusOS.</span><span class="sxs-lookup"><span data-stu-id="259da-118">This command creates an instance of SAP monitor by dictionary for PrometheusOS.</span></span>

### <span data-ttu-id="259da-119">Przykład 5: Tworzenie wystąpienia monitora protokołu SAP według słownika dla MsSqlServer</span><span class="sxs-lookup"><span data-stu-id="259da-119">Example 5: Create an instance of SAP monitor by dictionary for MsSqlServer</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-ms   -SapMonitorName dolauli-test04 -ProviderType MsSqlServer -InstanceProperty @{sqlHostname="10.4.8.90";sqlPort=1433;sqlUsername="AMFSS";sqlPassword="fakepassword"}

Name                Type
----                ----
dolauli-instance-ms Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="259da-120">To polecenie tworzy wystąpienie monitora protokołu SAP według słownika dla MsSqlServer.</span><span class="sxs-lookup"><span data-stu-id="259da-120">This command creates an instance of SAP monitor by dictionary for MsSqlServer.</span></span>

### <span data-ttu-id="259da-121">Przykład 6: Tworzenie wystąpienia monitora protokołu SAP według słownika dla SapHana</span><span class="sxs-lookup"><span data-stu-id="259da-121">Example 6: Create an instance of SAP monitor by dictionary for SapHana</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName donaliu-HN1 -Name dolauli-instance-hana   -SapMonitorName dolauli-test04 -ProviderType SapHana -InstanceProperty @{hanaHostname="10.1.2.6";hanaDbName="SYSTEMDB";hanaDbSqlPort=30113;hanaDbUsername="SYSTEM"; hanaDbPassword="Manager1"}

Name                  Type
----                  ----
dolauli-instance-hana Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="259da-122">To polecenie tworzy wystąpienie monitora protokołu SAP według słownika dla SapHana.</span><span class="sxs-lookup"><span data-stu-id="259da-122">This command creates an instance of SAP monitor by dictionary for SapHana.</span></span>

## <span data-ttu-id="259da-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="259da-123">PARAMETERS</span></span>

### <span data-ttu-id="259da-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="259da-124">-AsJob</span></span>
<span data-ttu-id="259da-125">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="259da-125">Run the command as a job</span></span>

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

### <span data-ttu-id="259da-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="259da-126">-DefaultProfile</span></span>
<span data-ttu-id="259da-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="259da-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="259da-128">-HanaDatabaseName</span><span class="sxs-lookup"><span data-stu-id="259da-128">-HanaDatabaseName</span></span>
<span data-ttu-id="259da-129">Nazwa bazy danych wystąpienia SAP HANA.</span><span class="sxs-lookup"><span data-stu-id="259da-129">The database name of SAP HANA instance.</span></span>

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

### <span data-ttu-id="259da-130">-HanaDatabasePassword</span><span class="sxs-lookup"><span data-stu-id="259da-130">-HanaDatabasePassword</span></span>
<span data-ttu-id="259da-131">Hasło do bazy danych wystąpienia SAP HANA.</span><span class="sxs-lookup"><span data-stu-id="259da-131">The password of the database of SAP HANA instance.</span></span>

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

### <span data-ttu-id="259da-132">-HanaDatabasePasswordKeyVaultResourceId</span><span class="sxs-lookup"><span data-stu-id="259da-132">-HanaDatabasePasswordKeyVaultResourceId</span></span>
<span data-ttu-id="259da-133">Identyfikator zasobu magazynu kluczy zawierającego poświadczenia HANA.</span><span class="sxs-lookup"><span data-stu-id="259da-133">Resource ID of the Key Vault that contains the HANA credentials.</span></span>

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

### <span data-ttu-id="259da-134">-HanaDatabasePasswordSecretId</span><span class="sxs-lookup"><span data-stu-id="259da-134">-HanaDatabasePasswordSecretId</span></span>
<span data-ttu-id="259da-135">Tajny identyfikator tajnego magazynu kluczy, który zawiera poświadczenia HANA.</span><span class="sxs-lookup"><span data-stu-id="259da-135">Secret identifier to the Key Vault secret that contains the HANA credentials.</span></span>

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

### <span data-ttu-id="259da-136">-HanaDatabaseSqlPort</span><span class="sxs-lookup"><span data-stu-id="259da-136">-HanaDatabaseSqlPort</span></span>
<span data-ttu-id="259da-137">Port SQL bazy danych wystąpienia SAP HANA.</span><span class="sxs-lookup"><span data-stu-id="259da-137">The SQL port of the database of SAP HANA instance.</span></span>

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

### <span data-ttu-id="259da-138">-HanaDatabaseUsername</span><span class="sxs-lookup"><span data-stu-id="259da-138">-HanaDatabaseUsername</span></span>
<span data-ttu-id="259da-139">Nazwa użytkownika bazy danych wystąpienia SAP HANA.</span><span class="sxs-lookup"><span data-stu-id="259da-139">The username of the database of SAP HANA instance.</span></span>

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

### <span data-ttu-id="259da-140">-HanaHostname</span><span class="sxs-lookup"><span data-stu-id="259da-140">-HanaHostname</span></span>
<span data-ttu-id="259da-141">Nazwa hosta wystąpienia SAP HANA.</span><span class="sxs-lookup"><span data-stu-id="259da-141">The hostname of SAP HANA instance.</span></span>

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

### <span data-ttu-id="259da-142">-InstanceProperty</span><span class="sxs-lookup"><span data-stu-id="259da-142">-InstanceProperty</span></span>
<span data-ttu-id="259da-143">Właściwość wystąpienia usługi HANA.</span><span class="sxs-lookup"><span data-stu-id="259da-143">The property of HANA instance.</span></span>

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

### <span data-ttu-id="259da-144">-Metadata</span><span class="sxs-lookup"><span data-stu-id="259da-144">-Metadata</span></span>
<span data-ttu-id="259da-145">Ciąg JSON zawierający metadane wystąpienia dostawcy.</span><span class="sxs-lookup"><span data-stu-id="259da-145">A JSON string containing metadata of the provider instance.</span></span>

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

### <span data-ttu-id="259da-146">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="259da-146">-Name</span></span>
<span data-ttu-id="259da-147">Nazwa wystąpienia dostawcy.</span><span class="sxs-lookup"><span data-stu-id="259da-147">Name of the provider instance.</span></span>

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

### <span data-ttu-id="259da-148">-Nowait</span><span class="sxs-lookup"><span data-stu-id="259da-148">-NoWait</span></span>
<span data-ttu-id="259da-149">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="259da-149">Run the command asynchronously</span></span>

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

### <span data-ttu-id="259da-150">-ProviderType</span><span class="sxs-lookup"><span data-stu-id="259da-150">-ProviderType</span></span>
<span data-ttu-id="259da-151">Typ wystąpienia dostawcy.</span><span class="sxs-lookup"><span data-stu-id="259da-151">The type of provider instance.</span></span>
<span data-ttu-id="259da-152">Obsługiwane wartości to: "SapHana".</span><span class="sxs-lookup"><span data-stu-id="259da-152">Supported values are: "SapHana".</span></span>

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

### <span data-ttu-id="259da-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="259da-153">-ResourceGroupName</span></span>
<span data-ttu-id="259da-154">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="259da-154">Name of the resource group.</span></span>

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

### <span data-ttu-id="259da-155">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="259da-155">-SapMonitorName</span></span>
<span data-ttu-id="259da-156">Nazwa zasobu monitorowania protokołu SAP.</span><span class="sxs-lookup"><span data-stu-id="259da-156">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="259da-157">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="259da-157">-SubscriptionId</span></span>
<span data-ttu-id="259da-158">Identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="259da-158">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="259da-159">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="259da-159">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="259da-160">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="259da-160">-Confirm</span></span>
<span data-ttu-id="259da-161">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="259da-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="259da-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="259da-162">-WhatIf</span></span>
<span data-ttu-id="259da-163">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="259da-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="259da-164">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="259da-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="259da-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="259da-165">CommonParameters</span></span>
<span data-ttu-id="259da-166">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="259da-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="259da-167">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="259da-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="259da-168">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="259da-168">INPUTS</span></span>

## <span data-ttu-id="259da-169">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="259da-169">OUTPUTS</span></span>

### <span data-ttu-id="259da-170">Microsoft. Azure. PowerShell. polecenia. HanaOnAzure. models. Api20200207Preview. IProviderInstance</span><span class="sxs-lookup"><span data-stu-id="259da-170">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span></span>

## <span data-ttu-id="259da-171">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="259da-171">NOTES</span></span>

<span data-ttu-id="259da-172">PISUJE</span><span class="sxs-lookup"><span data-stu-id="259da-172">ALIASES</span></span>

## <span data-ttu-id="259da-173">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="259da-173">RELATED LINKS</span></span>

