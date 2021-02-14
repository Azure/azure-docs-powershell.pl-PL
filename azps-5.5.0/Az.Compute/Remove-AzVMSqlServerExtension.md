---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
ms.openlocfilehash: 599b4817ce9f4f6f1f7a75f5811c5a3122f1bbb7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100244067"
---
# <span data-ttu-id="6431a-101">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="6431a-101">Remove-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="6431a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6431a-102">SYNOPSIS</span></span>
<span data-ttu-id="6431a-103">Usuwa rozszerzenie programu SQL Server z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6431a-103">Removes a SQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="6431a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6431a-104">SYNTAX</span></span>

```
Remove-AzVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6431a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="6431a-105">DESCRIPTION</span></span>
<span data-ttu-id="6431a-106">Polecenie **cmdlet Remove-AzVMSqlServerExtension** usuwa rozszerzenie AzureSQL Server z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6431a-106">The **Remove-AzVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="6431a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6431a-107">EXAMPLES</span></span>

### <span data-ttu-id="6431a-108">Przykład 1. Usuwanie rozszerzenia programu SQL Server</span><span class="sxs-lookup"><span data-stu-id="6431a-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="6431a-109">To polecenie usuwa rozszerzenie programu SQL Server z maszyny wirtualnej o nazwie ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="6431a-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="6431a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6431a-110">PARAMETERS</span></span>

### <span data-ttu-id="6431a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6431a-111">-DefaultProfile</span></span>
<span data-ttu-id="6431a-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6431a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6431a-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6431a-113">-Name</span></span>
<span data-ttu-id="6431a-114">Określa nazwę serwera SQL, które usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6431a-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6431a-115">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6431a-115">-NoWait</span></span>
<span data-ttu-id="6431a-116">Rozpoczyna operację i zwraca bezpośrednio przed jej ukończeniem.</span><span class="sxs-lookup"><span data-stu-id="6431a-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="6431a-117">Aby ustalić, czy operacja została pomyślnie ukończona, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="6431a-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="6431a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6431a-118">-ResourceGroupName</span></span>
<span data-ttu-id="6431a-119">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6431a-119">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6431a-120">-NAZWA.MASZYNY.WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="6431a-120">-VMName</span></span>
<span data-ttu-id="6431a-121">Określa nazwę maszyny wirtualnej, z której to polecenie cmdlet usuwa rozszerzenie programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6431a-121">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6431a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6431a-122">CommonParameters</span></span>
<span data-ttu-id="6431a-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6431a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6431a-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6431a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6431a-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6431a-125">INPUTS</span></span>

### <span data-ttu-id="6431a-126">System.String</span><span class="sxs-lookup"><span data-stu-id="6431a-126">System.String</span></span>

## <span data-ttu-id="6431a-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6431a-127">OUTPUTS</span></span>

### <span data-ttu-id="6431a-128">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="6431a-128">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="6431a-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6431a-129">NOTES</span></span>

## <span data-ttu-id="6431a-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6431a-130">RELATED LINKS</span></span>

[<span data-ttu-id="6431a-131">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="6431a-131">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="6431a-132">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="6431a-132">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


