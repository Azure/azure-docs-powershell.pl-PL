---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseWorkspace.md
ms.openlocfilehash: fb3613555e65b0d13650e5c15189edd865ab2b89
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340153"
---
# <span data-ttu-id="42a90-101">New-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="42a90-101">New-AzSynapseWorkspace</span></span>

## <span data-ttu-id="42a90-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="42a90-102">SYNOPSIS</span></span>
<span data-ttu-id="42a90-103">Umożliwia utworzenie obszaru roboczego analizy Synapse.</span><span class="sxs-lookup"><span data-stu-id="42a90-103">Creates a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="42a90-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="42a90-104">SYNTAX</span></span>

```
New-AzSynapseWorkspace -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 -DefaultDataLakeStorageAccountName <String> -DefaultDataLakeStorageFilesystem <String>
 -SqlAdministratorLoginCredential <PSCredential> [-ManagedVirtualNetwork <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42a90-105">Opis</span><span class="sxs-lookup"><span data-stu-id="42a90-105">DESCRIPTION</span></span>
<span data-ttu-id="42a90-106">Polecenie cmdlet **New-AzSynapseWorkspace** tworzy obszar roboczy funkcji Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="42a90-106">The **New-AzSynapseWorkspace** cmdlet creates an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="42a90-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="42a90-107">EXAMPLES</span></span>

### <span data-ttu-id="42a90-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="42a90-108">Example 1</span></span>
```powershell
PS C:\> $password = ConvertTo-SecureString "Password123!" -AsPlainText -Force
PS C:\> $creds = New-Object System.Management.Automation.PSCredential ("ContosoUser", $password)
PS C:\> New-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -Name ContosoWorkspace -Location northeurope -DefaultDataLakeStorageAccountName ContosoAdlGen2Storage -DefaultDataLakeStorageFilesystem ContosoFileSystem -SqlAdministratorLoginCredential $creds -AsJob
```

<span data-ttu-id="42a90-109">To polecenie tworzy obszar roboczy analizy Synapse o nazwie ContosoWorkspace, który używa ContosoAdlGenStorage magazynu danych w grupie zasobów o nazwie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="42a90-109">This command creates a Synapse Analytics workspace named ContosoWorkspace that uses the ContosoAdlGenStorage Data Store, in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="42a90-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="42a90-110">PARAMETERS</span></span>

### <span data-ttu-id="42a90-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="42a90-111">-AsJob</span></span>
<span data-ttu-id="42a90-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="42a90-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="42a90-113">-DefaultDataLakeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="42a90-113">-DefaultDataLakeStorageAccountName</span></span>
<span data-ttu-id="42a90-114">Domyślna nazwa konta ADLS Gen2 Storage.</span><span class="sxs-lookup"><span data-stu-id="42a90-114">The default ADLS Gen2 storage account name.</span></span>

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

### <span data-ttu-id="42a90-115">-DefaultDataLakeStorageFilesystem</span><span class="sxs-lookup"><span data-stu-id="42a90-115">-DefaultDataLakeStorageFilesystem</span></span>
<span data-ttu-id="42a90-116">Domyślny system plików ADLS Gen2.</span><span class="sxs-lookup"><span data-stu-id="42a90-116">The default ADLS Gen2 file system.</span></span>

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

### <span data-ttu-id="42a90-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42a90-117">-DefaultProfile</span></span>
<span data-ttu-id="42a90-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="42a90-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42a90-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="42a90-119">-Location</span></span>
<span data-ttu-id="42a90-120">Obszar platformy Azure, w którym ma zostać utworzony zasób.</span><span class="sxs-lookup"><span data-stu-id="42a90-120">Azure region where the resource should be created.</span></span>

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

### <span data-ttu-id="42a90-121">-ManagedVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="42a90-121">-ManagedVirtualNetwork</span></span>
<span data-ttu-id="42a90-122">Nazwa zarządzanej sieci wirtualnej Synapse dla obszaru roboczego usługi Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="42a90-122">Name of a Synapse-managed virtual network dedicated for the Azure Synapse workspace.</span></span>

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

### <span data-ttu-id="42a90-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="42a90-123">-Name</span></span>
<span data-ttu-id="42a90-124">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="42a90-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="42a90-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42a90-125">-ResourceGroupName</span></span>
<span data-ttu-id="42a90-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="42a90-126">Resource group name.</span></span>

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

### <span data-ttu-id="42a90-127">-SqlAdministratorLoginCredential</span><span class="sxs-lookup"><span data-stu-id="42a90-127">-SqlAdministratorLoginCredential</span></span>
<span data-ttu-id="42a90-128">Poświadczenia administratora SQL.</span><span class="sxs-lookup"><span data-stu-id="42a90-128">SQL administrator credentials.</span></span>

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

### <span data-ttu-id="42a90-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="42a90-129">-Tag</span></span>
<span data-ttu-id="42a90-130">Ciąg znaków, który jest ciągiem znaczników skojarzonych z zasobem.</span><span class="sxs-lookup"><span data-stu-id="42a90-130">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="42a90-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="42a90-131">-Confirm</span></span>
<span data-ttu-id="42a90-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42a90-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42a90-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42a90-133">-WhatIf</span></span>
<span data-ttu-id="42a90-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42a90-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42a90-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="42a90-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42a90-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42a90-136">CommonParameters</span></span>
<span data-ttu-id="42a90-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42a90-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42a90-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="42a90-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42a90-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="42a90-139">INPUTS</span></span>

### <span data-ttu-id="42a90-140">System. String</span><span class="sxs-lookup"><span data-stu-id="42a90-140">System.String</span></span>

### <span data-ttu-id="42a90-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="42a90-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="42a90-142">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="42a90-142">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="42a90-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="42a90-143">OUTPUTS</span></span>

### <span data-ttu-id="42a90-144">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="42a90-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="42a90-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="42a90-145">NOTES</span></span>

## <span data-ttu-id="42a90-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="42a90-146">RELATED LINKS</span></span>
