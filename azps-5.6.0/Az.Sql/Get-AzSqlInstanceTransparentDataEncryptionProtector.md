---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/Get-AzSqlInstanceTransparentDataEncryptionProtector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceTransparentDataEncryptionProtector.md
ms.openlocfilehash: 98538ba503b1fa31ae4c14897d56b0e0b9daffbc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999306"
---
# <span data-ttu-id="8c4f3-101">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="8c4f3-101">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="8c4f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c4f3-102">SYNOPSIS</span></span>
<span data-ttu-id="8c4f3-103">Pobiera szyfrowanie danych przezroczystych (TDE, Transparent Data Encryption) dla wystąpienia zarządzanego przez język SQL.</span><span class="sxs-lookup"><span data-stu-id="8c4f3-103">Gets the Transparent Data Encryption (TDE) protector for a SQL managed instance.</span></span>

## <span data-ttu-id="8c4f3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8c4f3-104">SYNTAX</span></span>

### <span data-ttu-id="8c4f3-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="8c4f3-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c4f3-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c4f3-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-Instance] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c4f3-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c4f3-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c4f3-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="8c4f3-108">DESCRIPTION</span></span>
<span data-ttu-id="8c4f3-109">Polecenie Get-AzSqlInstanceTransparentDataEncryptionProtector pobiera wartość TDE dla określonego wystąpienia zarządzanego przez język SQL.</span><span class="sxs-lookup"><span data-stu-id="8c4f3-109">The Get-AzSqlInstanceTransparentDataEncryptionProtector cmdlet gets the TDE protector for the specified SQL managed instance.</span></span>

## <span data-ttu-id="8c4f3-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8c4f3-110">EXAMPLES</span></span>

### <span data-ttu-id="8c4f3-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8c4f3-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="8c4f3-112">To polecenie pobiera nazwę TDE dla zarządzanego wystąpienia o nazwie ContosoManagedInstanceName w grupie zasobów o nazwie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8c4f3-112">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="8c4f3-113">Przykład 2. Używanie obiektu zarządzanego wystąpienia</span><span class="sxs-lookup"><span data-stu-id="8c4f3-113">Example 2: Using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -Instance $managedInstance 'ContosoManagedInstanceName'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="8c4f3-114">To polecenie pobiera nazwę TDE dla zarządzanego wystąpienia o nazwie ContosoManagedInstanceName w grupie zasobów o nazwie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8c4f3-114">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="8c4f3-115">Przykład 3. Używanie identyfikatora zasobu zarządzanego wystąpienia</span><span class="sxs-lookup"><span data-stu-id="8c4f3-115">Example 3: Using managed instance resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -InstanceResourceId $managedInstance.ResourceId

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="8c4f3-116">To polecenie pobiera nazwę TDE dla zarządzanego wystąpienia o nazwie ContosoManagedInstanceName w grupie zasobów o nazwie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8c4f3-116">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="8c4f3-117">Przykład 4. Stosowanie rur</span><span class="sxs-lookup"><span data-stu-id="8c4f3-117">Example 4: Using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Get-AzSqlInstanceTransparentDataEncryptionProtector

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="8c4f3-118">To polecenie pobiera nazwę TDE dla zarządzanego wystąpienia o nazwie ContosoManagedInstanceName w grupie zasobów o nazwie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8c4f3-118">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="8c4f3-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c4f3-119">PARAMETERS</span></span>

### <span data-ttu-id="8c4f3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c4f3-120">-DefaultProfile</span></span>
<span data-ttu-id="8c4f3-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8c4f3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c4f3-122">—Instance</span><span class="sxs-lookup"><span data-stu-id="8c4f3-122">-Instance</span></span>
<span data-ttu-id="8c4f3-123">Obiekt wejściowy wystąpienia</span><span class="sxs-lookup"><span data-stu-id="8c4f3-123">The instance input object</span></span>

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

### <span data-ttu-id="8c4f3-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="8c4f3-124">-InstanceName</span></span>
<span data-ttu-id="8c4f3-125">Nazwa wystąpienia</span><span class="sxs-lookup"><span data-stu-id="8c4f3-125">The instance name</span></span>

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

### <span data-ttu-id="8c4f3-126">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="8c4f3-126">-InstanceResourceId</span></span>
<span data-ttu-id="8c4f3-127">Identyfikator zasobu wystąpienia</span><span class="sxs-lookup"><span data-stu-id="8c4f3-127">The instance resource id</span></span>

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

### <span data-ttu-id="8c4f3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c4f3-128">-ResourceGroupName</span></span>
<span data-ttu-id="8c4f3-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="8c4f3-129">The Resource Group Name</span></span>

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

### <span data-ttu-id="8c4f3-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8c4f3-130">-Confirm</span></span>
<span data-ttu-id="8c4f3-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8c4f3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c4f3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c4f3-132">-WhatIf</span></span>
<span data-ttu-id="8c4f3-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c4f3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c4f3-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8c4f3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c4f3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c4f3-135">CommonParameters</span></span>
<span data-ttu-id="8c4f3-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c4f3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c4f3-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8c4f3-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c4f3-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8c4f3-138">INPUTS</span></span>

### <span data-ttu-id="8c4f3-139">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="8c4f3-139">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="8c4f3-140">System.String</span><span class="sxs-lookup"><span data-stu-id="8c4f3-140">System.String</span></span>

## <span data-ttu-id="8c4f3-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8c4f3-141">OUTPUTS</span></span>

### <span data-ttu-id="8c4f3-142">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="8c4f3-142">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="8c4f3-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8c4f3-143">NOTES</span></span>

## <span data-ttu-id="8c4f3-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8c4f3-144">RELATED LINKS</span></span>
