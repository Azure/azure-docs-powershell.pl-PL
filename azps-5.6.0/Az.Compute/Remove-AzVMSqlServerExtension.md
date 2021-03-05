---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
ms.openlocfilehash: 42fb10ef388fdda9616f78453163db822da9d036
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985223"
---
# <span data-ttu-id="06dc4-101">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="06dc4-101">Remove-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="06dc4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06dc4-102">SYNOPSIS</span></span>
<span data-ttu-id="06dc4-103">Usuwa rozszerzenie programu SQL Server z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="06dc4-103">Removes a SQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="06dc4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="06dc4-104">SYNTAX</span></span>

```
Remove-AzVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06dc4-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="06dc4-105">DESCRIPTION</span></span>
<span data-ttu-id="06dc4-106">Polecenie **cmdlet Remove-AzVMSqlServerExtension** usuwa rozszerzenie AzureSQL Server z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="06dc4-106">The **Remove-AzVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="06dc4-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="06dc4-107">EXAMPLES</span></span>

### <span data-ttu-id="06dc4-108">Przykład 1. Usuwanie rozszerzenia programu SQL Server</span><span class="sxs-lookup"><span data-stu-id="06dc4-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="06dc4-109">To polecenie usuwa rozszerzenie programu SQL Server z maszyny wirtualnej o nazwie ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="06dc4-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="06dc4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06dc4-110">PARAMETERS</span></span>

### <span data-ttu-id="06dc4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06dc4-111">-DefaultProfile</span></span>
<span data-ttu-id="06dc4-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="06dc4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06dc4-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="06dc4-113">-Name</span></span>
<span data-ttu-id="06dc4-114">Określa nazwę serwera SQL, które usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06dc4-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="06dc4-115">-NoWait</span><span class="sxs-lookup"><span data-stu-id="06dc4-115">-NoWait</span></span>
<span data-ttu-id="06dc4-116">Rozpoczyna operację i zwraca bezpośrednio przed jej ukończeniem.</span><span class="sxs-lookup"><span data-stu-id="06dc4-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="06dc4-117">Aby ustalić, czy operacja została pomyślnie ukończona, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="06dc4-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="06dc4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06dc4-118">-ResourceGroupName</span></span>
<span data-ttu-id="06dc4-119">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="06dc4-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="06dc4-120">-NAZWA.MASZYNY.WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="06dc4-120">-VMName</span></span>
<span data-ttu-id="06dc4-121">Określa nazwę maszyny wirtualnej, z której to polecenie cmdlet usuwa rozszerzenie programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="06dc4-121">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

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

### <span data-ttu-id="06dc4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06dc4-122">CommonParameters</span></span>
<span data-ttu-id="06dc4-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06dc4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06dc4-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="06dc4-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06dc4-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="06dc4-125">INPUTS</span></span>

### <span data-ttu-id="06dc4-126">System.String</span><span class="sxs-lookup"><span data-stu-id="06dc4-126">System.String</span></span>

## <span data-ttu-id="06dc4-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="06dc4-127">OUTPUTS</span></span>

### <span data-ttu-id="06dc4-128">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="06dc4-128">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="06dc4-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="06dc4-129">NOTES</span></span>

## <span data-ttu-id="06dc4-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="06dc4-130">RELATED LINKS</span></span>

[<span data-ttu-id="06dc4-131">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="06dc4-131">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="06dc4-132">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="06dc4-132">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


