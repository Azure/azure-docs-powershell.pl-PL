---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseWorkspace.md
ms.openlocfilehash: fb3613555e65b0d13650e5c15189edd865ab2b89
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195594"
---
# <span data-ttu-id="4788f-101">New-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="4788f-101">New-AzSynapseWorkspace</span></span>

## <span data-ttu-id="4788f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4788f-102">SYNOPSIS</span></span>
<span data-ttu-id="4788f-103">Tworzy obszar roboczy analizy Synapse.</span><span class="sxs-lookup"><span data-stu-id="4788f-103">Creates a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="4788f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4788f-104">SYNTAX</span></span>

```
New-AzSynapseWorkspace -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 -DefaultDataLakeStorageAccountName <String> -DefaultDataLakeStorageFilesystem <String>
 -SqlAdministratorLoginCredential <PSCredential> [-ManagedVirtualNetwork <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4788f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="4788f-105">DESCRIPTION</span></span>
<span data-ttu-id="4788f-106">Polecenie **cmdlet New-AzSynapseWorkspace** tworzy obszar roboczy usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="4788f-106">The **New-AzSynapseWorkspace** cmdlet creates an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="4788f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4788f-107">EXAMPLES</span></span>

### <span data-ttu-id="4788f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4788f-108">Example 1</span></span>
```powershell
PS C:\> $password = ConvertTo-SecureString "Password123!" -AsPlainText -Force
PS C:\> $creds = New-Object System.Management.Automation.PSCredential ("ContosoUser", $password)
PS C:\> New-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -Name ContosoWorkspace -Location northeurope -DefaultDataLakeStorageAccountName ContosoAdlGen2Storage -DefaultDataLakeStorageFilesystem ContosoFileSystem -SqlAdministratorLoginCredential $creds -AsJob
```

<span data-ttu-id="4788f-109">To polecenie tworzy obszar roboczy analizy Synapse o nazwie ContosoWorkspace, który korzysta ze sklepu danych ContosoAdlGenStorage, w grupie zasobów o nazwie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="4788f-109">This command creates a Synapse Analytics workspace named ContosoWorkspace that uses the ContosoAdlGenStorage Data Store, in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="4788f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4788f-110">PARAMETERS</span></span>

### <span data-ttu-id="4788f-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="4788f-111">-AsJob</span></span>
<span data-ttu-id="4788f-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="4788f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4788f-113">-DefaultDataLakeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4788f-113">-DefaultDataLakeStorageAccountName</span></span>
<span data-ttu-id="4788f-114">Domyślna nazwa konta magazynu usługi ADLS Gen2.</span><span class="sxs-lookup"><span data-stu-id="4788f-114">The default ADLS Gen2 storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4788f-115">-DefaultDataLakeStorageFilesystem</span><span class="sxs-lookup"><span data-stu-id="4788f-115">-DefaultDataLakeStorageFilesystem</span></span>
<span data-ttu-id="4788f-116">Domyślny system plików ADLS Gen2.</span><span class="sxs-lookup"><span data-stu-id="4788f-116">The default ADLS Gen2 file system.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4788f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4788f-117">-DefaultProfile</span></span>
<span data-ttu-id="4788f-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4788f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4788f-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="4788f-119">-Location</span></span>
<span data-ttu-id="4788f-120">Region platformy Azure, w którym należy utworzyć zasób.</span><span class="sxs-lookup"><span data-stu-id="4788f-120">Azure region where the resource should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4788f-121">-ManagedVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4788f-121">-ManagedVirtualNetwork</span></span>
<span data-ttu-id="4788f-122">Nazwa zarządzanej przez zespół Synapse sieci wirtualnej dedykowanej dla obszaru roboczego programu Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="4788f-122">Name of a Synapse-managed virtual network dedicated for the Azure Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: default

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4788f-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4788f-123">-Name</span></span>
<span data-ttu-id="4788f-124">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="4788f-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4788f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4788f-125">-ResourceGroupName</span></span>
<span data-ttu-id="4788f-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4788f-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4788f-127">-SqlAdministratorLoginCredential</span><span class="sxs-lookup"><span data-stu-id="4788f-127">-SqlAdministratorLoginCredential</span></span>
<span data-ttu-id="4788f-128">Poświadczenia administratora języka SQL.</span><span class="sxs-lookup"><span data-stu-id="4788f-128">SQL administrator credentials.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4788f-129">— Tag</span><span class="sxs-lookup"><span data-stu-id="4788f-129">-Tag</span></span>
<span data-ttu-id="4788f-130">A string,string dictionary of tags associated with the resource.</span><span class="sxs-lookup"><span data-stu-id="4788f-130">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4788f-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4788f-131">-Confirm</span></span>
<span data-ttu-id="4788f-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4788f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4788f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4788f-133">-WhatIf</span></span>
<span data-ttu-id="4788f-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4788f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4788f-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4788f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4788f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4788f-136">CommonParameters</span></span>
<span data-ttu-id="4788f-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4788f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4788f-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4788f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4788f-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4788f-139">INPUTS</span></span>

### <span data-ttu-id="4788f-140">System.String</span><span class="sxs-lookup"><span data-stu-id="4788f-140">System.String</span></span>

### <span data-ttu-id="4788f-141">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="4788f-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="4788f-142">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="4788f-142">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="4788f-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4788f-143">OUTPUTS</span></span>

### <span data-ttu-id="4788f-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="4788f-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="4788f-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4788f-145">NOTES</span></span>

## <span data-ttu-id="4788f-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4788f-146">RELATED LINKS</span></span>
