---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Set-AzSqlInstanceTransparentDataEncryptionProtector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceTransparentDataEncryptionProtector.md
ms.openlocfilehash: 15462ea79b5499818d71b145e0faaa35c09baf0b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499426"
---
# <span data-ttu-id="412f9-101">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="412f9-101">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="412f9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="412f9-102">SYNOPSIS</span></span>
<span data-ttu-id="412f9-103">Ustawia ochronę przezroczystego szyfrowania danych (TDE) dla wystąpienia zarządzanego SQL.</span><span class="sxs-lookup"><span data-stu-id="412f9-103">Sets the Transparent Data Encryption (TDE) protector for a SQL managed instance.</span></span>

## <span data-ttu-id="412f9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="412f9-104">SYNTAX</span></span>

### <span data-ttu-id="412f9-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="412f9-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (Default)</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-ResourceGroupName] <String> [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="412f9-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="412f9-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-Instance] <AzureSqlManagedInstanceModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="412f9-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="412f9-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-InstanceResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="412f9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="412f9-108">DESCRIPTION</span></span>
<span data-ttu-id="412f9-109">Polecenie cmdlet Set-AzSqlInstanceTransparentDataEncryptionProtector ustawia ochronę TDE dla wystąpienia zarządzanego przez SQL.</span><span class="sxs-lookup"><span data-stu-id="412f9-109">The Set-AzSqlInstanceTransparentDataEncryptionProtector cmdlet sets the TDE protector for a SQL managed instance.</span></span> <span data-ttu-id="412f9-110">Zmiana typu funkcji ochrony TDE spowoduje obrócenie funkcji ochrony.</span><span class="sxs-lookup"><span data-stu-id="412f9-110">Changing the TDE protector type will rotate the protector.</span></span>

## <span data-ttu-id="412f9-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="412f9-111">EXAMPLES</span></span>

### <span data-ttu-id="412f9-112">Przykład 1: Ustawianie przezroczystego typu szyfrowania danych (TDE) na servicemanage</span><span class="sxs-lookup"><span data-stu-id="412f9-112">Example 1: Set the Transparent Data Encryption (TDE) protector type to ServiceManaged</span></span>
```powershell
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -Type ServiceManaged

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : ServiceManaged
ManagedInstanceKeyVaultKeyName : ServiceManaged
KeyId                          :
```

<span data-ttu-id="412f9-113">To polecenie aktualizuje typ funkcji Ochrona TDEa zarządzanego wystąpienia, aby usługa była zarządzana.</span><span class="sxs-lookup"><span data-stu-id="412f9-113">This command updates a managed instance's TDE protector type to Service Managed.</span></span>

### <span data-ttu-id="412f9-114">Przykład 2: Ustawianie przezroczystego typu ochrony szyfrowania danych na magazyn kluczy platformy Azure</span><span class="sxs-lookup"><span data-stu-id="412f9-114">Example 2: Set the Transparent Data Encryption protector type to Azure Key Vault</span></span>
```powershell
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="412f9-115">To polecenie powoduje zaktualizowanie określonego wystąpienia zarządzanego za pomocą klucza magazynu kluczy wystąpienia zarządzanego o identyfikatorze " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 " jako funkcji ochrony TDE.</span><span class="sxs-lookup"><span data-stu-id="412f9-115">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="412f9-116">Przykład 3: Ustawianie przezroczystego typu ochrony szyfrowania danych do magazynu kluczy platformy Azure przy użyciu obiektu wystąpienia zarządzanego</span><span class="sxs-lookup"><span data-stu-id="412f9-116">Example 3: Set the Transparent Data Encryption protector type to Azure Key Vault using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -Instance $managedInstance -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="412f9-117">To polecenie powoduje zaktualizowanie określonego wystąpienia zarządzanego za pomocą klucza magazynu kluczy wystąpienia zarządzanego o identyfikatorze " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 " jako funkcji ochrony TDE.</span><span class="sxs-lookup"><span data-stu-id="412f9-117">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="412f9-118">Przykład 4: Ustawianie przezroczystego typu ochrony szyfrowania danych na magazyn kluczy Azure przy użyciu identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="412f9-118">Example 4: Set the Transparent Data Encryption protector type to Azure Key Vault using resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -InstanceResourceId $managedInstance.ResourceId -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="412f9-119">To polecenie powoduje zaktualizowanie określonego wystąpienia zarządzanego za pomocą klucza magazynu kluczy wystąpienia zarządzanego o identyfikatorze " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 " jako funkcji ochrony TDE.</span><span class="sxs-lookup"><span data-stu-id="412f9-119">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="412f9-120">Przykład 5: Ustawianie przezroczystego typu ochrony szyfrowania danych na magazyn kluczy Azure przy użyciu połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="412f9-120">Example 5: Set the Transparent Data Encryption protector type to Azure Key Vault using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Set-AzSqlInstanceTransparentDataEncryptionProtector -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="412f9-121">To polecenie powoduje zaktualizowanie określonego wystąpienia zarządzanego za pomocą klucza magazynu kluczy wystąpienia zarządzanego o identyfikatorze " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 " jako funkcji ochrony TDE.</span><span class="sxs-lookup"><span data-stu-id="412f9-121">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

## <span data-ttu-id="412f9-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="412f9-122">PARAMETERS</span></span>

### <span data-ttu-id="412f9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="412f9-123">-DefaultProfile</span></span>
<span data-ttu-id="412f9-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="412f9-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="412f9-125">-Force</span><span class="sxs-lookup"><span data-stu-id="412f9-125">-Force</span></span>
<span data-ttu-id="412f9-126">Pomiń komunikat potwierdzający wykonanie akcji</span><span class="sxs-lookup"><span data-stu-id="412f9-126">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="412f9-127">-Instance</span><span class="sxs-lookup"><span data-stu-id="412f9-127">-Instance</span></span>
<span data-ttu-id="412f9-128">Obiekt wejściowy wystąpienia</span><span class="sxs-lookup"><span data-stu-id="412f9-128">The instance input object</span></span>

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

### <span data-ttu-id="412f9-129">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="412f9-129">-InstanceName</span></span>
<span data-ttu-id="412f9-130">Nazwa wystąpienia</span><span class="sxs-lookup"><span data-stu-id="412f9-130">The instance name</span></span>

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

### <span data-ttu-id="412f9-131">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="412f9-131">-InstanceResourceId</span></span>
<span data-ttu-id="412f9-132">Identyfikator zasobu wystąpienia</span><span class="sxs-lookup"><span data-stu-id="412f9-132">The instance resource id</span></span>

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

### <span data-ttu-id="412f9-133">-KeyId</span><span class="sxs-lookup"><span data-stu-id="412f9-133">-KeyId</span></span>
<span data-ttu-id="412f9-134">Usługa Magazyn kluczy platformy Azure KeyId.</span><span class="sxs-lookup"><span data-stu-id="412f9-134">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="412f9-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="412f9-135">-ResourceGroupName</span></span>
<span data-ttu-id="412f9-136">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="412f9-136">The Resource Group Name</span></span>

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

### <span data-ttu-id="412f9-137">-Type</span><span class="sxs-lookup"><span data-stu-id="412f9-137">-Type</span></span>
<span data-ttu-id="412f9-138">Typ ochrony szyfrowania danych przezroczystość bazy danych usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="412f9-138">The Azure Sql Database Transparent Data Encryption Protector type.</span></span>

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

### <span data-ttu-id="412f9-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="412f9-139">-Confirm</span></span>
<span data-ttu-id="412f9-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="412f9-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="412f9-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="412f9-141">-WhatIf</span></span>
<span data-ttu-id="412f9-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="412f9-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="412f9-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="412f9-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="412f9-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="412f9-144">CommonParameters</span></span>
<span data-ttu-id="412f9-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="412f9-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="412f9-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="412f9-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="412f9-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="412f9-147">INPUTS</span></span>

### <span data-ttu-id="412f9-148">Microsoft. Azure. Commands. SQL. ManagedInstance. model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="412f9-148">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="412f9-149">System. String</span><span class="sxs-lookup"><span data-stu-id="412f9-149">System.String</span></span>

## <span data-ttu-id="412f9-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="412f9-150">OUTPUTS</span></span>

### <span data-ttu-id="412f9-151">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. model. AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="412f9-151">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="412f9-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="412f9-152">NOTES</span></span>

## <span data-ttu-id="412f9-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="412f9-153">RELATED LINKS</span></span>
