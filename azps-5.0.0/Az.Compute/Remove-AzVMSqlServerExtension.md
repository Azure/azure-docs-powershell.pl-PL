---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
ms.openlocfilehash: 599b4817ce9f4f6f1f7a75f5811c5a3122f1bbb7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318655"
---
# <span data-ttu-id="c6bf9-101">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="c6bf9-101">Remove-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="c6bf9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c6bf9-102">SYNOPSIS</span></span>
<span data-ttu-id="c6bf9-103">Usuwa rozszerzenie programu SQL Server z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c6bf9-103">Removes a SQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="c6bf9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c6bf9-104">SYNTAX</span></span>

```
Remove-AzVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6bf9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c6bf9-105">DESCRIPTION</span></span>
<span data-ttu-id="c6bf9-106">Polecenie cmdlet **Remove-AzVMSqlServerExtension** usuwa rozszerzenie serwera AzureSQL z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c6bf9-106">The **Remove-AzVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="c6bf9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c6bf9-107">EXAMPLES</span></span>

### <span data-ttu-id="c6bf9-108">Przykład 1: Usuwanie rozszerzenia programu SQL Server</span><span class="sxs-lookup"><span data-stu-id="c6bf9-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="c6bf9-109">To polecenie usuwa rozszerzenie programu SQL Server z maszyny wirtualnej o nazwie ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="c6bf9-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="c6bf9-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c6bf9-110">PARAMETERS</span></span>

### <span data-ttu-id="c6bf9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6bf9-111">-DefaultProfile</span></span>
<span data-ttu-id="c6bf9-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c6bf9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6bf9-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c6bf9-113">-Name</span></span>
<span data-ttu-id="c6bf9-114">Określa nazwę rozszerzenia programu SQL Server, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6bf9-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c6bf9-115">-Nowait</span><span class="sxs-lookup"><span data-stu-id="c6bf9-115">-NoWait</span></span>
<span data-ttu-id="c6bf9-116">Rozpoczyna operację i wraca natychmiast, zanim operacja zostanie ukończona.</span><span class="sxs-lookup"><span data-stu-id="c6bf9-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="c6bf9-117">W celu ustalenia, czy operacja została wykonana pomyślnie, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="c6bf9-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="c6bf9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6bf9-118">-ResourceGroupName</span></span>
<span data-ttu-id="c6bf9-119">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c6bf9-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="c6bf9-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="c6bf9-120">-VMName</span></span>
<span data-ttu-id="c6bf9-121">Określa nazwę maszyny wirtualnej, z której to polecenie cmdlet usuwa rozszerzenie programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c6bf9-121">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

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

### <span data-ttu-id="c6bf9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6bf9-122">CommonParameters</span></span>
<span data-ttu-id="c6bf9-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6bf9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6bf9-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c6bf9-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6bf9-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c6bf9-125">INPUTS</span></span>

### <span data-ttu-id="c6bf9-126">System. String</span><span class="sxs-lookup"><span data-stu-id="c6bf9-126">System.String</span></span>

## <span data-ttu-id="c6bf9-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c6bf9-127">OUTPUTS</span></span>

### <span data-ttu-id="c6bf9-128">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="c6bf9-128">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="c6bf9-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c6bf9-129">NOTES</span></span>

## <span data-ttu-id="c6bf9-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c6bf9-130">RELATED LINKS</span></span>

[<span data-ttu-id="c6bf9-131">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="c6bf9-131">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="c6bf9-132">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="c6bf9-132">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


