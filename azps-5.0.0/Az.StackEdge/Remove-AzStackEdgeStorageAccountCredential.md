---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: 1a55a8c08182ae4a32e27bec74e4a5870aae95fa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317532"
---
# <span data-ttu-id="6ff42-101">Remove-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="6ff42-101">Remove-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="6ff42-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6ff42-102">SYNOPSIS</span></span>
<span data-ttu-id="6ff42-103">Usuwa poświadczenia konta magazynu dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="6ff42-103">Removes a storage account credential for a device.</span></span>

## <span data-ttu-id="6ff42-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6ff42-104">SYNTAX</span></span>

### <span data-ttu-id="6ff42-105">DeleteByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6ff42-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6ff42-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ff42-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccountCredential [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ff42-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ff42-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccountCredential [-InputObject] <PSStackEdgeStorageAccountCredential> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ff42-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6ff42-108">DESCRIPTION</span></span>
<span data-ttu-id="6ff42-109">Polecenie cmdlet **Remove-AzStackEdgeStorageAccountCredential** usuwa poświadczenia konta magazynu dla urządzenia z krawędzią stosu.</span><span class="sxs-lookup"><span data-stu-id="6ff42-109">The **Remove-AzStackEdgeStorageAccountCredential** cmdlet removes the storage account credential for a Stack Edge device.</span></span>

## <span data-ttu-id="6ff42-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6ff42-110">EXAMPLES</span></span>

### <span data-ttu-id="6ff42-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6ff42-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeStorageAccountCredential ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAccountCredentialName
```

## <span data-ttu-id="6ff42-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6ff42-112">PARAMETERS</span></span>

### <span data-ttu-id="6ff42-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6ff42-113">-AsJob</span></span>
<span data-ttu-id="6ff42-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="6ff42-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6ff42-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ff42-115">-DefaultProfile</span></span>
<span data-ttu-id="6ff42-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6ff42-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ff42-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="6ff42-117">-DeviceName</span></span>
<span data-ttu-id="6ff42-118">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="6ff42-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ff42-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6ff42-119">-InputObject</span></span>
<span data-ttu-id="6ff42-120">Obiekt wejściowy</span><span class="sxs-lookup"><span data-stu-id="6ff42-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: StorageAccountCredential

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ff42-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6ff42-121">-Name</span></span>
<span data-ttu-id="6ff42-122">Nazwa konta magazynu, które ma być używane</span><span class="sxs-lookup"><span data-stu-id="6ff42-122">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: StorageAccountCredentialName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ff42-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6ff42-123">-PassThru</span></span>
<span data-ttu-id="6ff42-124">Zwraca wartość PRAWDA, jeśli powodzenie</span><span class="sxs-lookup"><span data-stu-id="6ff42-124">returns true if successful</span></span>

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

### <span data-ttu-id="6ff42-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ff42-125">-ResourceGroupName</span></span>
<span data-ttu-id="6ff42-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="6ff42-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ff42-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ff42-127">-ResourceId</span></span>
<span data-ttu-id="6ff42-128">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="6ff42-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ff42-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6ff42-129">-Confirm</span></span>
<span data-ttu-id="6ff42-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ff42-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ff42-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ff42-131">-WhatIf</span></span>
<span data-ttu-id="6ff42-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ff42-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6ff42-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6ff42-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ff42-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ff42-134">CommonParameters</span></span>
<span data-ttu-id="6ff42-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ff42-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ff42-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6ff42-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ff42-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6ff42-137">INPUTS</span></span>

### <span data-ttu-id="6ff42-138">System. String</span><span class="sxs-lookup"><span data-stu-id="6ff42-138">System.String</span></span>

### <span data-ttu-id="6ff42-139">Microsoft. Azure. PowerShell. polecenia. StackEdge. models. PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="6ff42-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="6ff42-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6ff42-140">OUTPUTS</span></span>

### <span data-ttu-id="6ff42-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6ff42-141">System.Boolean</span></span>

## <span data-ttu-id="6ff42-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6ff42-142">NOTES</span></span>

## <span data-ttu-id="6ff42-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6ff42-143">RELATED LINKS</span></span>
