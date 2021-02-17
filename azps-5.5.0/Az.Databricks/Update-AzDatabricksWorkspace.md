---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/update-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksWorkspace.md
ms.openlocfilehash: 0d213dd18ea2423c90dec6446e4551cbcd8d161a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198042"
---
# <span data-ttu-id="10f52-101">Update-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="10f52-101">Update-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="10f52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10f52-102">SYNOPSIS</span></span>
<span data-ttu-id="10f52-103">Aktualizuje obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="10f52-103">Updates a workspace.</span></span>

## <span data-ttu-id="10f52-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="10f52-104">SYNTAX</span></span>

### <span data-ttu-id="10f52-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="10f52-105">UpdateExpanded (Default)</span></span>
```
Update-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EncryptionKeyName <String>] [-EncryptionKeySource <KeySource>] [-EncryptionKeyVaultUri <String>]
 [-EncryptionKeyVersion <String>] [-PrepareEncryption] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="10f52-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="10f52-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-EncryptionKeyName <String>]
 [-EncryptionKeySource <KeySource>] [-EncryptionKeyVaultUri <String>] [-EncryptionKeyVersion <String>]
 [-PrepareEncryption] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="10f52-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="10f52-107">DESCRIPTION</span></span>
<span data-ttu-id="10f52-108">Aktualizuje obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="10f52-108">Updates a workspace.</span></span>

## <span data-ttu-id="10f52-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="10f52-109">EXAMPLES</span></span>

### <span data-ttu-id="10f52-110">Przykład 1. Aktualizacja tagów obszaru roboczego programu Databricks</span><span class="sxs-lookup"><span data-stu-id="10f52-110">Example 1: Updates the tags of a Databricks workspace</span></span>
```powershell
PS C:\> $dbr = Get-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceopsc46 -Tag @{'key'=1}
PS C:\> Update-AzDatabricksWorkspace -InputObject $dbr -Tag @{key="value"}

Name            Location Managed Resource Group ID
----            -------- -------------------------
workspaceopsc46 eastus   /subscriptions/0140911e-1040-48da-8bc9-b99fb3dd88a6/resourceGroups/databricks-rg-workspaceopsc46-wfgp3ayhu6jkn
```

<span data-ttu-id="10f52-111">To polecenie aktualizuje tagi obszaru roboczego programu Databricks.</span><span class="sxs-lookup"><span data-stu-id="10f52-111">This command updates the tags of a Databricks workspace.</span></span>

### <span data-ttu-id="10f52-112">Przykład 2. Włączanie szyfrowania w obszarze roboczym programu Databricks</span><span class="sxs-lookup"><span data-stu-id="10f52-112">Example 2: Enable encryption on a Databricks workspace</span></span>
```powershell
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -PrepareEncryption
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -EncryptionKeySource 'Microsoft.KeyVault' -EncryptionKeyVaultUri https://keyvalult-j3kube.vault.azure.net/ -EncryptionKeyName key-p3bjsf -EncryptionKeyVersion 853999da89714fb4a1408681945135fd

Name            Location       Managed Resource Group ID
----            --------       -------------------------
workspaceypae6l East US 2 EUAP /subscriptions/0140911e-1040-48da-8bc9-b99fb3dd88a6/resourceGroups/databricks-rg-workspaceypae6l-wzefrgv2b075t
```

<span data-ttu-id="10f52-113">Włączenie szyfrowania w obszarze roboczym programu Databricks wymaga trzech kroków:</span><span class="sxs-lookup"><span data-stu-id="10f52-113">Enabling encryption on a Databricks workspace takes three steps:</span></span>
1.
<span data-ttu-id="10f52-114">Zaktualizuj obszar roboczy `-PrepareEncryption` (jeśli tak nie został utworzony).</span><span class="sxs-lookup"><span data-stu-id="10f52-114">Update the workspace with `-PrepareEncryption` (if it was not created so).</span></span>
1.
<span data-ttu-id="10f52-115">Znajdź `StorageAccountIdentityPrincipalId` w wyniku ostatniego kroku.</span><span class="sxs-lookup"><span data-stu-id="10f52-115">Find `StorageAccountIdentityPrincipalId` in the output of the last step.</span></span>
<span data-ttu-id="10f52-116">Udzielanie głównych uprawnień podmiotowi zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="10f52-116">Grant key permissions to the principal.</span></span>
1.
<span data-ttu-id="10f52-117">Zaktualizuj ponownie obszar roboczy, aby wypełnić informacje o kluczu szyfrowania:</span><span class="sxs-lookup"><span data-stu-id="10f52-117">Update the workspace again to fill in information about the encryption key:</span></span>
    - `-EncryptionKeySource`
    - `-EncryptionKeyVaultUri`
    - `-EncryptionKeyName`
    - `-EncryptionKeyVersion`

### <span data-ttu-id="10f52-118">Przykład 3. Wyłączanie szyfrowania w obszarze roboczym usługi Databricks</span><span class="sxs-lookup"><span data-stu-id="10f52-118">Example 3: Disable encryption on a Databricks workspace</span></span>
```powershell
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -EncryptionKeySource 'Default'
```

<span data-ttu-id="10f52-119">Aby wyłączyć szyfrowanie, wystarczy ustawić `-EncryptionKeySource` wartość `'Default'` .</span><span class="sxs-lookup"><span data-stu-id="10f52-119">To disable encryption, simply set `-EncryptionKeySource` to `'Default'`.</span></span>

## <span data-ttu-id="10f52-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10f52-120">PARAMETERS</span></span>

### <span data-ttu-id="10f52-121">— AsJob</span><span class="sxs-lookup"><span data-stu-id="10f52-121">-AsJob</span></span>
<span data-ttu-id="10f52-122">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="10f52-122">Run the command as a job</span></span>

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

### <span data-ttu-id="10f52-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10f52-123">-DefaultProfile</span></span>
<span data-ttu-id="10f52-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="10f52-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10f52-125">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="10f52-125">-EncryptionKeyName</span></span>
<span data-ttu-id="10f52-126">Nazwa klucza magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="10f52-126">The name of Key Vault key.</span></span>

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

### <span data-ttu-id="10f52-127">-EncryptionKeySource</span><span class="sxs-lookup"><span data-stu-id="10f52-127">-EncryptionKeySource</span></span>
<span data-ttu-id="10f52-128">Klucz szyfrowaniaSource (provider).</span><span class="sxs-lookup"><span data-stu-id="10f52-128">The encryption keySource (provider).</span></span>
<span data-ttu-id="10f52-129">Możliwe wartości (bez uwzględniania liter): Domyślne, Microsoft.Keyvault</span><span class="sxs-lookup"><span data-stu-id="10f52-129">Possible values (case-insensitive): Default, Microsoft.Keyvault</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Support.KeySource
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10f52-130">-EncryptionKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="10f52-130">-EncryptionKeyVaultUri</span></span>
<span data-ttu-id="10f52-131">URI (nazwa DNS) magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="10f52-131">The URI (DNS name) of the Key Vault.</span></span>

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

### <span data-ttu-id="10f52-132">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="10f52-132">-EncryptionKeyVersion</span></span>
<span data-ttu-id="10f52-133">Wersja klawisza KeyVault.</span><span class="sxs-lookup"><span data-stu-id="10f52-133">The version of KeyVault key.</span></span>

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

### <span data-ttu-id="10f52-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10f52-134">-InputObject</span></span>
<span data-ttu-id="10f52-135">Parametr tożsamości.</span><span class="sxs-lookup"><span data-stu-id="10f52-135">Identity parameter.</span></span>
<span data-ttu-id="10f52-136">Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach inputOBJECT i utworzyć tabelę skrótów.</span><span class="sxs-lookup"><span data-stu-id="10f52-136">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10f52-137">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="10f52-137">-Name</span></span>
<span data-ttu-id="10f52-138">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="10f52-138">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10f52-139">-NoWait</span><span class="sxs-lookup"><span data-stu-id="10f52-139">-NoWait</span></span>
<span data-ttu-id="10f52-140">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="10f52-140">Run the command asynchronously</span></span>

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

### <span data-ttu-id="10f52-141">- PrepareEncryption</span><span class="sxs-lookup"><span data-stu-id="10f52-141">-PrepareEncryption</span></span>
<span data-ttu-id="10f52-142">Przygotowywanie obszaru roboczego do szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="10f52-142">Prepare the workspace for encryption.</span></span>
<span data-ttu-id="10f52-143">Włącza tożsamość zarządzaną dla konta magazynu zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="10f52-143">Enables the Managed Identity for managed storage account.</span></span>

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

### <span data-ttu-id="10f52-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10f52-144">-ResourceGroupName</span></span>
<span data-ttu-id="10f52-145">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="10f52-145">The name of the resource group.</span></span>
<span data-ttu-id="10f52-146">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="10f52-146">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10f52-147">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="10f52-147">-SubscriptionId</span></span>
<span data-ttu-id="10f52-148">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="10f52-148">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10f52-149">— Tag</span><span class="sxs-lookup"><span data-stu-id="10f52-149">-Tag</span></span>
<span data-ttu-id="10f52-150">Tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="10f52-150">Resource tags.</span></span>

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

### <span data-ttu-id="10f52-151">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="10f52-151">-Confirm</span></span>
<span data-ttu-id="10f52-152">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="10f52-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10f52-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10f52-153">-WhatIf</span></span>
<span data-ttu-id="10f52-154">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10f52-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10f52-155">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="10f52-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10f52-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10f52-156">CommonParameters</span></span>
<span data-ttu-id="10f52-157">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10f52-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10f52-158">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="10f52-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10f52-159">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10f52-159">INPUTS</span></span>

### <span data-ttu-id="10f52-160">Microsoft.Azure.PowerShell.Cmdlet.Databricks.Models.IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="10f52-160">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="10f52-161">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10f52-161">OUTPUTS</span></span>

### <span data-ttu-id="10f52-162">Microsoft.Azure.PowerShell.Cmdlet.Databricks.Models.Api20180401.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="10f52-162">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="10f52-163">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="10f52-163">NOTES</span></span>

<span data-ttu-id="10f52-164">ALIASY</span><span class="sxs-lookup"><span data-stu-id="10f52-164">ALIASES</span></span>

<span data-ttu-id="10f52-165">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="10f52-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="10f52-166">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="10f52-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="10f52-167">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="10f52-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="10f52-168">INPUTOBJECT: <IDatabricksIdentity> Parametr tożsamości.</span><span class="sxs-lookup"><span data-stu-id="10f52-168">INPUTOBJECT <IDatabricksIdentity>: Identity parameter.</span></span>
  - <span data-ttu-id="10f52-169">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="10f52-169">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="10f52-170">`[PeeringName <String>]`: nazwa komunikacji równorzędnej vNet obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="10f52-170">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="10f52-171">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="10f52-171">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="10f52-172">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="10f52-172">The name is case insensitive.</span></span>
  - <span data-ttu-id="10f52-173">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="10f52-173">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="10f52-174">`[WorkspaceName <String>]`: nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="10f52-174">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="10f52-175">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="10f52-175">RELATED LINKS</span></span>

