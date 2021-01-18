---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/remove-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVM.md
ms.openlocfilehash: 4478ec96cd7354a404a736ddd0f305cba5675b26
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98498241"
---
# <span data-ttu-id="ec4e0-101">Remove-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="ec4e0-101">Remove-AzSqlVM</span></span>

## <span data-ttu-id="ec4e0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ec4e0-102">SYNOPSIS</span></span>
<span data-ttu-id="ec4e0-103">Umożliwia usunięcie maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="ec4e0-103">Deletes a sql virtual machine.</span></span>

## <span data-ttu-id="ec4e0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ec4e0-104">SYNTAX</span></span>

### <span data-ttu-id="ec4e0-105">Nazwa (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="ec4e0-105">Name (Default)</span></span>
```
Remove-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec4e0-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="ec4e0-106">InputObject</span></span>
```
Remove-AzSqlVM [-InputObject] <AzureSqlVMModel> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec4e0-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="ec4e0-107">ResourceId</span></span>
```
Remove-AzSqlVM [-ResourceId] <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec4e0-108">Opis</span><span class="sxs-lookup"><span data-stu-id="ec4e0-108">DESCRIPTION</span></span>
<span data-ttu-id="ec4e0-109">Polecenie cmdlet Remove-AzSqlVM powoduje usunięcie maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="ec4e0-109">The Remove-AzSqlVM cmdlet deletes a sql virtual machine.</span></span>

## <span data-ttu-id="ec4e0-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ec4e0-110">EXAMPLES</span></span>

### <span data-ttu-id="ec4e0-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ec4e0-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm"
```

<span data-ttu-id="ec4e0-112">Usuwa maszynę wirtualną SQL Azure "VM" w grupie zasobów ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="ec4e0-112">Deletes the Azure SQL virtual machine "vm" in the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="ec4e0-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ec4e0-113">PARAMETERS</span></span>

### <span data-ttu-id="ec4e0-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ec4e0-114">-AsJob</span></span>
<span data-ttu-id="ec4e0-115">Uruchom polecenie cmdlet w tle.</span><span class="sxs-lookup"><span data-stu-id="ec4e0-115">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="ec4e0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec4e0-116">-DefaultProfile</span></span>
<span data-ttu-id="ec4e0-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ec4e0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec4e0-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ec4e0-118">-InputObject</span></span>
<span data-ttu-id="ec4e0-119">Obiekt maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="ec4e0-119">SQL virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel
Parameter Sets: InputObject
Aliases: SqlVM

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec4e0-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ec4e0-120">-Name</span></span>
<span data-ttu-id="ec4e0-121">Nazwa maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="ec4e0-121">SQL virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: SqlVMName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec4e0-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ec4e0-122">-PassThru</span></span>
<span data-ttu-id="ec4e0-123">Określa, czy usunięty zasób ma być wyprowadzany na końcu wykonania polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec4e0-123">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="ec4e0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec4e0-124">-ResourceGroupName</span></span>
<span data-ttu-id="ec4e0-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ec4e0-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec4e0-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec4e0-126">-ResourceId</span></span>
<span data-ttu-id="ec4e0-127">Identyfikator zasobu maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="ec4e0-127">SQL virtual machine resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: SqlVMId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec4e0-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ec4e0-128">-Confirm</span></span>
<span data-ttu-id="ec4e0-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec4e0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec4e0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec4e0-130">-WhatIf</span></span>
<span data-ttu-id="ec4e0-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec4e0-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec4e0-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ec4e0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec4e0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec4e0-133">CommonParameters</span></span>
<span data-ttu-id="ec4e0-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec4e0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec4e0-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ec4e0-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec4e0-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ec4e0-136">INPUTS</span></span>

### <span data-ttu-id="ec4e0-137">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="ec4e0-137">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="ec4e0-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ec4e0-138">OUTPUTS</span></span>

### <span data-ttu-id="ec4e0-139">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="ec4e0-139">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="ec4e0-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ec4e0-140">NOTES</span></span>

## <span data-ttu-id="ec4e0-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ec4e0-141">RELATED LINKS</span></span>
