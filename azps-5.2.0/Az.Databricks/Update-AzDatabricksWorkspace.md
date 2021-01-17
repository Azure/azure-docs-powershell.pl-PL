---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/update-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksWorkspace.md
ms.openlocfilehash: 0d213dd18ea2423c90dec6446e4551cbcd8d161a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365981"
---
# <span data-ttu-id="375cc-101">Update-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="375cc-101">Update-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="375cc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="375cc-102">SYNOPSIS</span></span>
<span data-ttu-id="375cc-103">Aktualizowanie obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="375cc-103">Updates a workspace.</span></span>

## <span data-ttu-id="375cc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="375cc-104">SYNTAX</span></span>

### <span data-ttu-id="375cc-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="375cc-105">UpdateExpanded (Default)</span></span>
```
Update-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EncryptionKeyName <String>] [-EncryptionKeySource <KeySource>] [-EncryptionKeyVaultUri <String>]
 [-EncryptionKeyVersion <String>] [-PrepareEncryption] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="375cc-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="375cc-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-EncryptionKeyName <String>]
 [-EncryptionKeySource <KeySource>] [-EncryptionKeyVaultUri <String>] [-EncryptionKeyVersion <String>]
 [-PrepareEncryption] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="375cc-107">Opis</span><span class="sxs-lookup"><span data-stu-id="375cc-107">DESCRIPTION</span></span>
<span data-ttu-id="375cc-108">Aktualizowanie obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="375cc-108">Updates a workspace.</span></span>

## <span data-ttu-id="375cc-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="375cc-109">EXAMPLES</span></span>

### <span data-ttu-id="375cc-110">Przykład 1. a aktualizuje Tagi obszaru roboczego datakostki</span><span class="sxs-lookup"><span data-stu-id="375cc-110">Example 1: Updates the tags of a Databricks workspace</span></span>
```powershell
PS C:\> $dbr = Get-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceopsc46 -Tag @{'key'=1}
PS C:\> Update-AzDatabricksWorkspace -InputObject $dbr -Tag @{key="value"}

Name            Location Managed Resource Group ID
----            -------- -------------------------
workspaceopsc46 eastus   /subscriptions/0140911e-1040-48da-8bc9-b99fb3dd88a6/resourceGroups/databricks-rg-workspaceopsc46-wfgp3ayhu6jkn
```

<span data-ttu-id="375cc-111">To polecenie aktualizuje Tagi obszaru roboczego datakostki.</span><span class="sxs-lookup"><span data-stu-id="375cc-111">This command updates the tags of a Databricks workspace.</span></span>

### <span data-ttu-id="375cc-112">Przykład 2: Włączanie szyfrowania w obszarze roboczym datakostki</span><span class="sxs-lookup"><span data-stu-id="375cc-112">Example 2: Enable encryption on a Databricks workspace</span></span>
```powershell
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -PrepareEncryption
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -EncryptionKeySource 'Microsoft.KeyVault' -EncryptionKeyVaultUri https://keyvalult-j3kube.vault.azure.net/ -EncryptionKeyName key-p3bjsf -EncryptionKeyVersion 853999da89714fb4a1408681945135fd

Name            Location       Managed Resource Group ID
----            --------       -------------------------
workspaceypae6l East US 2 EUAP /subscriptions/0140911e-1040-48da-8bc9-b99fb3dd88a6/resourceGroups/databricks-rg-workspaceypae6l-wzefrgv2b075t
```

<span data-ttu-id="375cc-113">Włączenie szyfrowania w obszarze roboczym datakostki wymaga wykonania trzech kroków:</span><span class="sxs-lookup"><span data-stu-id="375cc-113">Enabling encryption on a Databricks workspace takes three steps:</span></span>
1.
<span data-ttu-id="375cc-114">Aktualizowanie obszaru roboczego za pomocą `-PrepareEncryption` (jeśli nie został utworzony).</span><span class="sxs-lookup"><span data-stu-id="375cc-114">Update the workspace with `-PrepareEncryption` (if it was not created so).</span></span>
1.
<span data-ttu-id="375cc-115">Znajdź `StorageAccountIdentityPrincipalId` w wyniku ostatniego kroku.</span><span class="sxs-lookup"><span data-stu-id="375cc-115">Find `StorageAccountIdentityPrincipalId` in the output of the last step.</span></span>
<span data-ttu-id="375cc-116">Udzielanie kluczowych uprawnień podmiotowi zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="375cc-116">Grant key permissions to the principal.</span></span>
1.
<span data-ttu-id="375cc-117">Ponownie zaktualizuj obszar roboczy, aby wypełnić informacje o kluczu szyfrowania:</span><span class="sxs-lookup"><span data-stu-id="375cc-117">Update the workspace again to fill in information about the encryption key:</span></span>
    - `-EncryptionKeySource`
    - `-EncryptionKeyVaultUri`
    - `-EncryptionKeyName`
    - `-EncryptionKeyVersion`

### <span data-ttu-id="375cc-118">Przykład 3: wyłączanie szyfrowania w obszarze roboczym datakostki</span><span class="sxs-lookup"><span data-stu-id="375cc-118">Example 3: Disable encryption on a Databricks workspace</span></span>
```powershell
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -EncryptionKeySource 'Default'
```

<span data-ttu-id="375cc-119">Aby wyłączyć szyfrowanie, należy po prostu ustawić pozycję `-EncryptionKeySource` `'Default'` .</span><span class="sxs-lookup"><span data-stu-id="375cc-119">To disable encryption, simply set `-EncryptionKeySource` to `'Default'`.</span></span>

## <span data-ttu-id="375cc-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="375cc-120">PARAMETERS</span></span>

### <span data-ttu-id="375cc-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="375cc-121">-AsJob</span></span>
<span data-ttu-id="375cc-122">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="375cc-122">Run the command as a job</span></span>

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

### <span data-ttu-id="375cc-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="375cc-123">-DefaultProfile</span></span>
<span data-ttu-id="375cc-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="375cc-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="375cc-125">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="375cc-125">-EncryptionKeyName</span></span>
<span data-ttu-id="375cc-126">Nazwa klucza magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="375cc-126">The name of Key Vault key.</span></span>

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

### <span data-ttu-id="375cc-127">-EncryptionKeySource</span><span class="sxs-lookup"><span data-stu-id="375cc-127">-EncryptionKeySource</span></span>
<span data-ttu-id="375cc-128">Źródło klucza szyfrowania (dostawca).</span><span class="sxs-lookup"><span data-stu-id="375cc-128">The encryption keySource (provider).</span></span>
<span data-ttu-id="375cc-129">Możliwe wartości (bez uwzględniania wielkości liter): domyślny, Microsoft. datamagazyn</span><span class="sxs-lookup"><span data-stu-id="375cc-129">Possible values (case-insensitive): Default, Microsoft.Keyvault</span></span>

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

### <span data-ttu-id="375cc-130">-EncryptionKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="375cc-130">-EncryptionKeyVaultUri</span></span>
<span data-ttu-id="375cc-131">Identyfikator URI (nazwa DNS) magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="375cc-131">The URI (DNS name) of the Key Vault.</span></span>

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

### <span data-ttu-id="375cc-132">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="375cc-132">-EncryptionKeyVersion</span></span>
<span data-ttu-id="375cc-133">Wersja klucza magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="375cc-133">The version of KeyVault key.</span></span>

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

### <span data-ttu-id="375cc-134">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="375cc-134">-InputObject</span></span>
<span data-ttu-id="375cc-135">Parametr Identity.</span><span class="sxs-lookup"><span data-stu-id="375cc-135">Identity parameter.</span></span>
<span data-ttu-id="375cc-136">Aby skonstruować, zobacz sekcję notatki dla właściwości INPUTobject i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="375cc-136">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="375cc-137">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="375cc-137">-Name</span></span>
<span data-ttu-id="375cc-138">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="375cc-138">The name of the workspace.</span></span>

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

### <span data-ttu-id="375cc-139">-Nowait</span><span class="sxs-lookup"><span data-stu-id="375cc-139">-NoWait</span></span>
<span data-ttu-id="375cc-140">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="375cc-140">Run the command asynchronously</span></span>

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

### <span data-ttu-id="375cc-141">-PrepareEncryption</span><span class="sxs-lookup"><span data-stu-id="375cc-141">-PrepareEncryption</span></span>
<span data-ttu-id="375cc-142">Przygotuj obszar roboczy do szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="375cc-142">Prepare the workspace for encryption.</span></span>
<span data-ttu-id="375cc-143">Umożliwia administrowanie tożsamością zarządzanych kont magazynu.</span><span class="sxs-lookup"><span data-stu-id="375cc-143">Enables the Managed Identity for managed storage account.</span></span>

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

### <span data-ttu-id="375cc-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="375cc-144">-ResourceGroupName</span></span>
<span data-ttu-id="375cc-145">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="375cc-145">The name of the resource group.</span></span>
<span data-ttu-id="375cc-146">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="375cc-146">The name is case insensitive.</span></span>

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

### <span data-ttu-id="375cc-147">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="375cc-147">-SubscriptionId</span></span>
<span data-ttu-id="375cc-148">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="375cc-148">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="375cc-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="375cc-149">-Tag</span></span>
<span data-ttu-id="375cc-150">Znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="375cc-150">Resource tags.</span></span>

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

### <span data-ttu-id="375cc-151">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="375cc-151">-Confirm</span></span>
<span data-ttu-id="375cc-152">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="375cc-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="375cc-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="375cc-153">-WhatIf</span></span>
<span data-ttu-id="375cc-154">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="375cc-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="375cc-155">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="375cc-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="375cc-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="375cc-156">CommonParameters</span></span>
<span data-ttu-id="375cc-157">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="375cc-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="375cc-158">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="375cc-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="375cc-159">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="375cc-159">INPUTS</span></span>

### <span data-ttu-id="375cc-160">Microsoft. Azure. PowerShell. polecenia. datakosteks. models. IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="375cc-160">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="375cc-161">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="375cc-161">OUTPUTS</span></span>

### <span data-ttu-id="375cc-162">Microsoft. Azure. PowerShell. polecenia. datakosteks. models. Api20180401. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="375cc-162">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="375cc-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="375cc-163">NOTES</span></span>

<span data-ttu-id="375cc-164">PISUJE</span><span class="sxs-lookup"><span data-stu-id="375cc-164">ALIASES</span></span>

<span data-ttu-id="375cc-165">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="375cc-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="375cc-166">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="375cc-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="375cc-167">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="375cc-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="375cc-168">INPUTobject <IDatabricksIdentity> : parametr Identity.</span><span class="sxs-lookup"><span data-stu-id="375cc-168">INPUTOBJECT <IDatabricksIdentity>: Identity parameter.</span></span>
  - <span data-ttu-id="375cc-169">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="375cc-169">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="375cc-170">`[PeeringName <String>]`: Nazwa komunikacji równorzędnej w obszarze roboczym w sieci vNet.</span><span class="sxs-lookup"><span data-stu-id="375cc-170">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="375cc-171">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="375cc-171">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="375cc-172">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="375cc-172">The name is case insensitive.</span></span>
  - <span data-ttu-id="375cc-173">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="375cc-173">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="375cc-174">`[WorkspaceName <String>]`: Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="375cc-174">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="375cc-175">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="375cc-175">RELATED LINKS</span></span>

