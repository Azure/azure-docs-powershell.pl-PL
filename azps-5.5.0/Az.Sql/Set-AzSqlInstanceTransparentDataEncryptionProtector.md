---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Set-AzSqlInstanceTransparentDataEncryptionProtector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceTransparentDataEncryptionProtector.md
ms.openlocfilehash: 15462ea79b5499818d71b145e0faaa35c09baf0b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195938"
---
# <span data-ttu-id="bc20b-101">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="bc20b-101">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="bc20b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc20b-102">SYNOPSIS</span></span>
<span data-ttu-id="bc20b-103">Ustawia szyfrowanie danych przezroczystych (TDE, Transparent Data Encryption) dla wystąpienia zarządzanego przez język SQL.</span><span class="sxs-lookup"><span data-stu-id="bc20b-103">Sets the Transparent Data Encryption (TDE) protector for a SQL managed instance.</span></span>

## <span data-ttu-id="bc20b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bc20b-104">SYNTAX</span></span>

### <span data-ttu-id="bc20b-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="bc20b-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (Default)</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-ResourceGroupName] <String> [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc20b-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc20b-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-Instance] <AzureSqlManagedInstanceModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc20b-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc20b-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-InstanceResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bc20b-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="bc20b-108">DESCRIPTION</span></span>
<span data-ttu-id="bc20b-109">To Set-AzSqlInstanceTransparentDataEncryptionProtector cmdlet ustawia amortyzkę TDE dla wystąpienia zarządzanego przez język SQL.</span><span class="sxs-lookup"><span data-stu-id="bc20b-109">The Set-AzSqlInstanceTransparentDataEncryptionProtector cmdlet sets the TDE protector for a SQL managed instance.</span></span> <span data-ttu-id="bc20b-110">Zmiana typu TDE spowoduje zmianę tego rodzaju ustawień.</span><span class="sxs-lookup"><span data-stu-id="bc20b-110">Changing the TDE protector type will rotate the protector.</span></span>

## <span data-ttu-id="bc20b-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bc20b-111">EXAMPLES</span></span>

### <span data-ttu-id="bc20b-112">Przykład 1. Ustawianie typu danych transparentne szyfrowanie danych (TDE) na wartość ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="bc20b-112">Example 1: Set the Transparent Data Encryption (TDE) protector type to ServiceManaged</span></span>
```powershell
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -Type ServiceManaged

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : ServiceManaged
ManagedInstanceKeyVaultKeyName : ServiceManaged
KeyId                          :
```

<span data-ttu-id="bc20b-113">To polecenie aktualizuje typ danych TDE zarządzanego wystąpienia na typ Service Managed (Zarządzane usługi).</span><span class="sxs-lookup"><span data-stu-id="bc20b-113">This command updates a managed instance's TDE protector type to Service Managed.</span></span>

### <span data-ttu-id="bc20b-114">Przykład 2. Ustawianie typu szyfrowania danych przezroczystych na magazyn kluczy platformy Azure</span><span class="sxs-lookup"><span data-stu-id="bc20b-114">Example 2: Set the Transparent Data Encryption protector type to Azure Key Vault</span></span>
```powershell
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="bc20b-115">To polecenie aktualizuje określone wystąpienie zarządzane, aby używać klucza magazynu klucza zarządzanego wystąpienia z https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 identyfikatorem ' jako klucza TDE.</span><span class="sxs-lookup"><span data-stu-id="bc20b-115">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="bc20b-116">Przykład 3. Ustawianie typu szyfrowania danych przezroczystych na magazyn kluczy platformy Azure przy użyciu obiektu wystąpienia zarządzanego</span><span class="sxs-lookup"><span data-stu-id="bc20b-116">Example 3: Set the Transparent Data Encryption protector type to Azure Key Vault using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -Instance $managedInstance -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="bc20b-117">To polecenie aktualizuje określone wystąpienie zarządzane, aby używać klucza magazynu klucza zarządzanego wystąpienia z https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 identyfikatorem ' jako klucza TDE.</span><span class="sxs-lookup"><span data-stu-id="bc20b-117">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="bc20b-118">Przykład 4. Ustawianie typu szyfrowania danych przezroczystych na magazyn kluczy platformy Azure przy użyciu identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="bc20b-118">Example 4: Set the Transparent Data Encryption protector type to Azure Key Vault using resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -InstanceResourceId $managedInstance.ResourceId -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="bc20b-119">To polecenie aktualizuje określone wystąpienie zarządzane, aby używać klucza magazynu klucza zarządzanego wystąpienia z https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 identyfikatorem ' jako klucza TDE.</span><span class="sxs-lookup"><span data-stu-id="bc20b-119">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="bc20b-120">Przykład 5. Ustawianie typu szyfrowania danych przezroczystych na magazyn kluczy platformy Azure za pomocą rur</span><span class="sxs-lookup"><span data-stu-id="bc20b-120">Example 5: Set the Transparent Data Encryption protector type to Azure Key Vault using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Set-AzSqlInstanceTransparentDataEncryptionProtector -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="bc20b-121">To polecenie aktualizuje określone wystąpienie zarządzane, aby używać klucza magazynu klucza zarządzanego wystąpienia z https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 identyfikatorem ' jako klucza TDE.</span><span class="sxs-lookup"><span data-stu-id="bc20b-121">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

## <span data-ttu-id="bc20b-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc20b-122">PARAMETERS</span></span>

### <span data-ttu-id="bc20b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc20b-123">-DefaultProfile</span></span>
<span data-ttu-id="bc20b-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bc20b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc20b-125">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="bc20b-125">-Force</span></span>
<span data-ttu-id="bc20b-126">Pomiń komunikat potwierdzenia wykonania akcji</span><span class="sxs-lookup"><span data-stu-id="bc20b-126">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="bc20b-127">—Instance</span><span class="sxs-lookup"><span data-stu-id="bc20b-127">-Instance</span></span>
<span data-ttu-id="bc20b-128">Obiekt wejściowy wystąpienia</span><span class="sxs-lookup"><span data-stu-id="bc20b-128">The instance input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet
Aliases: InputObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc20b-129">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="bc20b-129">-InstanceName</span></span>
<span data-ttu-id="bc20b-130">Nazwa wystąpienia</span><span class="sxs-lookup"><span data-stu-id="bc20b-130">The instance name</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc20b-131">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="bc20b-131">-InstanceResourceId</span></span>
<span data-ttu-id="bc20b-132">Identyfikator zasobu wystąpienia</span><span class="sxs-lookup"><span data-stu-id="bc20b-132">The instance resource id</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc20b-133">-KeyId</span><span class="sxs-lookup"><span data-stu-id="bc20b-133">-KeyId</span></span>
<span data-ttu-id="bc20b-134">Azure KeyId (Klucz klucza klucza platformy Azure).</span><span class="sxs-lookup"><span data-stu-id="bc20b-134">The Azure Key Vault KeyId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc20b-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc20b-135">-ResourceGroupName</span></span>
<span data-ttu-id="bc20b-136">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="bc20b-136">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc20b-137">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="bc20b-137">-Type</span></span>
<span data-ttu-id="bc20b-138">Typ szyfrowania przezroczystych danych bazy danych Azure Sql Database.</span><span class="sxs-lookup"><span data-stu-id="bc20b-138">The Azure Sql Database Transparent Data Encryption Protector type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType
Parameter Sets: (All)
Aliases:
Accepted values: AzureKeyVault, ServiceManaged

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc20b-139">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bc20b-139">-Confirm</span></span>
<span data-ttu-id="bc20b-140">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bc20b-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc20b-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc20b-141">-WhatIf</span></span>
<span data-ttu-id="bc20b-142">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc20b-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc20b-143">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="bc20b-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc20b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc20b-144">CommonParameters</span></span>
<span data-ttu-id="bc20b-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc20b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc20b-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bc20b-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc20b-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bc20b-147">INPUTS</span></span>

### <span data-ttu-id="bc20b-148">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="bc20b-148">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="bc20b-149">System.String</span><span class="sxs-lookup"><span data-stu-id="bc20b-149">System.String</span></span>

## <span data-ttu-id="bc20b-150">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bc20b-150">OUTPUTS</span></span>

### <span data-ttu-id="bc20b-151">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="bc20b-151">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="bc20b-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bc20b-152">NOTES</span></span>

## <span data-ttu-id="bc20b-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bc20b-153">RELATED LINKS</span></span>
