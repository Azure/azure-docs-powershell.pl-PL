---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/new-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitorProviderInstance.md
ms.openlocfilehash: f0d8486bc26043ee4f2cb2126c7ffdc64829a7cd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224306"
---
# <span data-ttu-id="fe048-101">New-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="fe048-101">New-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="fe048-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fe048-102">SYNOPSIS</span></span>
<span data-ttu-id="fe048-103">Tworzy wystąpienie dostawcy dla określonej subskrypcji, grupy zasobów, nazwy SapMonitor i nazwy zasobu.</span><span class="sxs-lookup"><span data-stu-id="fe048-103">Creates a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="fe048-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fe048-104">SYNTAX</span></span>

### <span data-ttu-id="fe048-105">ByString (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fe048-105">ByString (Default)</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -HanaDatabaseName <String> -HanaDatabasePassword <SecureString> -HanaDatabaseSqlPort <Int32>
 -HanaDatabaseUsername <String> -HanaHostname <String> -ProviderType <String> [-SubscriptionId <String>]
 [-Metadata <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="fe048-106">ByKeyVault</span><span class="sxs-lookup"><span data-stu-id="fe048-106">ByKeyVault</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -HanaDatabaseName <String> -HanaDatabasePasswordKeyVaultResourceId <String>
 -HanaDatabasePasswordSecretId <String> -HanaDatabaseSqlPort <Int32> -HanaDatabaseUsername <String>
 -HanaHostname <String> -ProviderType <String> [-SubscriptionId <String>] [-Metadata <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fe048-107">Opis</span><span class="sxs-lookup"><span data-stu-id="fe048-107">DESCRIPTION</span></span>
<span data-ttu-id="fe048-108">Tworzy wystąpienie dostawcy dla określonej subskrypcji, grupy zasobów, nazwy SapMonitor i nazwy zasobu.</span><span class="sxs-lookup"><span data-stu-id="fe048-108">Creates a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="fe048-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fe048-109">EXAMPLES</span></span>

### <span data-ttu-id="fe048-110">Przykład 1. Tworzenie wystąpienia monitora protokołu SAP według ciągu dla HANA</span><span class="sxs-lookup"><span data-stu-id="fe048-110">Example 1: Create an instance of SAP monitor by string for HANA</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -Name ps-sapmonitorins-t01 -SapMonitorName yemingmonitor -ProviderType SapHana -HanaHostname 'hdb1-0' -HanaDatabaseName 'SYSTEMDB' -HanaDatabaseSqlPort 30015 -HanaDatabaseUsername SYSTEM -HanaDatabasePassword (ConvertTo-SecureString "Manager1" -AsPlainText -Force)

Name                 Type
----                 ----
ps-sapmonitorins-t01 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="fe048-111">To polecenie tworzy wystąpienie monitora protokołu SAP według ciągu dla obiektu HANA.</span><span class="sxs-lookup"><span data-stu-id="fe048-111">This command creates an instance of SAP monitor by string for HANA.</span></span>

### <span data-ttu-id="fe048-112">Przykład 2: Tworzenie wystąpienia monitora protokołu SAP według magazynu kluczy dla HANA</span><span class="sxs-lookup"><span data-stu-id="fe048-112">Example 2: Create an instance of SAP monitor by key vault for HANA</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName sapMonitor-vayh7q-test -ProviderType SapHana -HanaHostname 'hdb1-0' -HanaDatabaseName 'SYSTEMDB' -HanaDatabaseSqlPort 30015 -HanaDatabaseUsername SYSTEM -HanaDatabasePasswordSecretId https://kv-9gosjc-test.vault.azure.net/secrets/hanaPassword/bf516d1dfcc144138e5cf55114f3344b -HanaDatabasePasswordKeyVaultResourceId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/costmanagement-rg-8p50xe/providers/Microsoft.KeyVault/vaults/kv-9gosjc-test -Name sapins-kv-test

Name           Type
----           ----
sapins-kv-test Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="fe048-113">To polecenie tworzy wystąpienie monitora protokołu SAP według magazynu kluczy dla HANA.</span><span class="sxs-lookup"><span data-stu-id="fe048-113">This command creates an instance of SAP monitor by key vault for HANA.</span></span>

## <span data-ttu-id="fe048-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fe048-114">PARAMETERS</span></span>

### <span data-ttu-id="fe048-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fe048-115">-AsJob</span></span>
<span data-ttu-id="fe048-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="fe048-116">Run the command as a job</span></span>

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

### <span data-ttu-id="fe048-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe048-117">-DefaultProfile</span></span>
<span data-ttu-id="fe048-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fe048-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe048-119">-HanaDatabaseName</span><span class="sxs-lookup"><span data-stu-id="fe048-119">-HanaDatabaseName</span></span>
<span data-ttu-id="fe048-120">Nazwa bazy danych wystąpienia SAP HANA.</span><span class="sxs-lookup"><span data-stu-id="fe048-120">The database name of SAP HANA instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HanaDbName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe048-121">-HanaDatabasePassword</span><span class="sxs-lookup"><span data-stu-id="fe048-121">-HanaDatabasePassword</span></span>
<span data-ttu-id="fe048-122">Hasło do bazy danych wystąpienia SAP HANA.</span><span class="sxs-lookup"><span data-stu-id="fe048-122">The password of the database of SAP HANA instance.</span></span>

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

### <span data-ttu-id="fe048-123">-HanaDatabasePasswordKeyVaultResourceId</span><span class="sxs-lookup"><span data-stu-id="fe048-123">-HanaDatabasePasswordKeyVaultResourceId</span></span>
<span data-ttu-id="fe048-124">Identyfikator zasobu magazynu kluczy zawierającego poświadczenia HANA.</span><span class="sxs-lookup"><span data-stu-id="fe048-124">Resource ID of the Key Vault that contains the HANA credentials.</span></span>

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

### <span data-ttu-id="fe048-125">-HanaDatabasePasswordSecretId</span><span class="sxs-lookup"><span data-stu-id="fe048-125">-HanaDatabasePasswordSecretId</span></span>
<span data-ttu-id="fe048-126">Tajny identyfikator tajnego magazynu kluczy, który zawiera poświadczenia HANA.</span><span class="sxs-lookup"><span data-stu-id="fe048-126">Secret identifier to the Key Vault secret that contains the HANA credentials.</span></span>

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

### <span data-ttu-id="fe048-127">-HanaDatabaseSqlPort</span><span class="sxs-lookup"><span data-stu-id="fe048-127">-HanaDatabaseSqlPort</span></span>
<span data-ttu-id="fe048-128">Port SQL bazy danych wystąpienia SAP HANA.</span><span class="sxs-lookup"><span data-stu-id="fe048-128">The SQL port of the database of SAP HANA instance.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: HanaDbSqlPort

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe048-129">-HanaDatabaseUsername</span><span class="sxs-lookup"><span data-stu-id="fe048-129">-HanaDatabaseUsername</span></span>
<span data-ttu-id="fe048-130">Nazwa użytkownika bazy danych wystąpienia SAP HANA.</span><span class="sxs-lookup"><span data-stu-id="fe048-130">The username of the database of SAP HANA instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HanaDbUsername

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe048-131">-HanaHostname</span><span class="sxs-lookup"><span data-stu-id="fe048-131">-HanaHostname</span></span>
<span data-ttu-id="fe048-132">Nazwa hosta wystąpienia SAP HANA.</span><span class="sxs-lookup"><span data-stu-id="fe048-132">The hostname of SAP HANA instance.</span></span>

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

### <span data-ttu-id="fe048-133">-Metadata</span><span class="sxs-lookup"><span data-stu-id="fe048-133">-Metadata</span></span>
<span data-ttu-id="fe048-134">Ciąg JSON zawierający metadane wystąpienia dostawcy.</span><span class="sxs-lookup"><span data-stu-id="fe048-134">A JSON string containing metadata of the provider instance.</span></span>

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

### <span data-ttu-id="fe048-135">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fe048-135">-Name</span></span>
<span data-ttu-id="fe048-136">Nazwa wystąpienia dostawcy.</span><span class="sxs-lookup"><span data-stu-id="fe048-136">Name of the provider instance.</span></span>

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

### <span data-ttu-id="fe048-137">-Nowait</span><span class="sxs-lookup"><span data-stu-id="fe048-137">-NoWait</span></span>
<span data-ttu-id="fe048-138">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="fe048-138">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fe048-139">-ProviderType</span><span class="sxs-lookup"><span data-stu-id="fe048-139">-ProviderType</span></span>
<span data-ttu-id="fe048-140">Typ wystąpienia dostawcy.</span><span class="sxs-lookup"><span data-stu-id="fe048-140">The type of provider instance.</span></span>
<span data-ttu-id="fe048-141">Obsługiwane wartości to: "SapHana".</span><span class="sxs-lookup"><span data-stu-id="fe048-141">Supported values are: "SapHana".</span></span>

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

### <span data-ttu-id="fe048-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe048-142">-ResourceGroupName</span></span>
<span data-ttu-id="fe048-143">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fe048-143">Name of the resource group.</span></span>

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

### <span data-ttu-id="fe048-144">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="fe048-144">-SapMonitorName</span></span>
<span data-ttu-id="fe048-145">Nazwa zasobu monitorowania protokołu SAP.</span><span class="sxs-lookup"><span data-stu-id="fe048-145">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="fe048-146">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="fe048-146">-SubscriptionId</span></span>
<span data-ttu-id="fe048-147">Identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="fe048-147">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="fe048-148">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="fe048-148">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="fe048-149">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fe048-149">-Confirm</span></span>
<span data-ttu-id="fe048-150">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe048-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe048-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe048-151">-WhatIf</span></span>
<span data-ttu-id="fe048-152">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe048-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe048-153">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fe048-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe048-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe048-154">CommonParameters</span></span>
<span data-ttu-id="fe048-155">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe048-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe048-156">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fe048-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe048-157">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe048-157">INPUTS</span></span>

## <span data-ttu-id="fe048-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fe048-158">OUTPUTS</span></span>

### <span data-ttu-id="fe048-159">Microsoft. Azure. PowerShell. polecenia. HanaOnAzure. models. Api20200207Preview. IProviderInstance</span><span class="sxs-lookup"><span data-stu-id="fe048-159">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span></span>

## <span data-ttu-id="fe048-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fe048-160">NOTES</span></span>

<span data-ttu-id="fe048-161">PISUJE</span><span class="sxs-lookup"><span data-stu-id="fe048-161">ALIASES</span></span>

## <span data-ttu-id="fe048-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fe048-162">RELATED LINKS</span></span>

