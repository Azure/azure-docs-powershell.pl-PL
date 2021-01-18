---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Get-AzSqlInstanceTransparentDataEncryptionProtector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceTransparentDataEncryptionProtector.md
ms.openlocfilehash: 8307581d1e3627be5cb2ab9fc146327342ced187
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499801"
---
# <span data-ttu-id="45c37-101">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="45c37-101">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="45c37-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="45c37-102">SYNOPSIS</span></span>
<span data-ttu-id="45c37-103">Pobiera funkcję ochrony przezroczystego szyfrowania danych (TDE) dla wystąpienia zarządzanego SQL.</span><span class="sxs-lookup"><span data-stu-id="45c37-103">Gets the Transparent Data Encryption (TDE) protector for a SQL managed instance.</span></span>

## <span data-ttu-id="45c37-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="45c37-104">SYNTAX</span></span>

### <span data-ttu-id="45c37-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="45c37-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45c37-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="45c37-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-Instance] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45c37-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="45c37-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45c37-108">Opis</span><span class="sxs-lookup"><span data-stu-id="45c37-108">DESCRIPTION</span></span>
<span data-ttu-id="45c37-109">Polecenie cmdlet Get-AzSqlInstanceTransparentDataEncryptionProtector pobiera ochronę TDE dla określonego wystąpienia zarządzanego SQL.</span><span class="sxs-lookup"><span data-stu-id="45c37-109">The Get-AzSqlInstanceTransparentDataEncryptionProtector cmdlet gets the TDE protector for the specified SQL managed instance.</span></span>

## <span data-ttu-id="45c37-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="45c37-110">EXAMPLES</span></span>

### <span data-ttu-id="45c37-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="45c37-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="45c37-112">To polecenie pobiera ochronę TDE dla wystąpienia zarządzanego o nazwie ContosoManagedInstanceName w grupie zasobów o nazwie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="45c37-112">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="45c37-113">Przykład 2: Używanie obiektu wystąpienia zarządzanego</span><span class="sxs-lookup"><span data-stu-id="45c37-113">Example 2: Using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -Instance $managedInstance 'ContosoManagedInstanceName'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="45c37-114">To polecenie pobiera ochronę TDE dla wystąpienia zarządzanego o nazwie ContosoManagedInstanceName w grupie zasobów o nazwie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="45c37-114">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="45c37-115">Przykład 3: używanie identyfikatora zasobu wystąpienia zarządzanego</span><span class="sxs-lookup"><span data-stu-id="45c37-115">Example 3: Using managed instance resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -InstanceResourceId $managedInstance.ResourceId

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="45c37-116">To polecenie pobiera ochronę TDE dla wystąpienia zarządzanego o nazwie ContosoManagedInstanceName w grupie zasobów o nazwie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="45c37-116">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="45c37-117">Przykład 4: korzystanie z połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="45c37-117">Example 4: Using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Get-AzSqlInstanceTransparentDataEncryptionProtector

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="45c37-118">To polecenie pobiera ochronę TDE dla wystąpienia zarządzanego o nazwie ContosoManagedInstanceName w grupie zasobów o nazwie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="45c37-118">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="45c37-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="45c37-119">PARAMETERS</span></span>

### <span data-ttu-id="45c37-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45c37-120">-DefaultProfile</span></span>
<span data-ttu-id="45c37-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="45c37-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45c37-122">-Instance</span><span class="sxs-lookup"><span data-stu-id="45c37-122">-Instance</span></span>
<span data-ttu-id="45c37-123">Obiekt wejściowy wystąpienia</span><span class="sxs-lookup"><span data-stu-id="45c37-123">The instance input object</span></span>

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

### <span data-ttu-id="45c37-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="45c37-124">-InstanceName</span></span>
<span data-ttu-id="45c37-125">Nazwa wystąpienia</span><span class="sxs-lookup"><span data-stu-id="45c37-125">The instance name</span></span>

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

### <span data-ttu-id="45c37-126">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="45c37-126">-InstanceResourceId</span></span>
<span data-ttu-id="45c37-127">Identyfikator zasobu wystąpienia</span><span class="sxs-lookup"><span data-stu-id="45c37-127">The instance resource id</span></span>

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

### <span data-ttu-id="45c37-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45c37-128">-ResourceGroupName</span></span>
<span data-ttu-id="45c37-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="45c37-129">The Resource Group Name</span></span>

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

### <span data-ttu-id="45c37-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="45c37-130">-Confirm</span></span>
<span data-ttu-id="45c37-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45c37-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45c37-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45c37-132">-WhatIf</span></span>
<span data-ttu-id="45c37-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45c37-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45c37-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="45c37-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45c37-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45c37-135">CommonParameters</span></span>
<span data-ttu-id="45c37-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45c37-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45c37-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="45c37-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45c37-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="45c37-138">INPUTS</span></span>

### <span data-ttu-id="45c37-139">Microsoft. Azure. Commands. SQL. ManagedInstance. model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="45c37-139">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="45c37-140">System. String</span><span class="sxs-lookup"><span data-stu-id="45c37-140">System.String</span></span>

## <span data-ttu-id="45c37-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="45c37-141">OUTPUTS</span></span>

### <span data-ttu-id="45c37-142">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. model. AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="45c37-142">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="45c37-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="45c37-143">NOTES</span></span>

## <span data-ttu-id="45c37-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="45c37-144">RELATED LINKS</span></span>
