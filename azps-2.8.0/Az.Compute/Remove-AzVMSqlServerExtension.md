---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
ms.openlocfilehash: 81acbdd914d4a3cdb69da9ac0d2093f4e1dd4cdf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706250"
---
# <span data-ttu-id="04d20-101">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="04d20-101">Remove-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="04d20-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="04d20-102">SYNOPSIS</span></span>
<span data-ttu-id="04d20-103">Usuwa rozszerzenie programu SQL Server z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="04d20-103">Removes a SQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="04d20-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="04d20-104">SYNTAX</span></span>

```
Remove-AzVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04d20-105">Opis</span><span class="sxs-lookup"><span data-stu-id="04d20-105">DESCRIPTION</span></span>
<span data-ttu-id="04d20-106">Polecenie cmdlet **Remove-AzVMSqlServerExtension** usuwa rozszerzenie serwera AzureSQL z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="04d20-106">The **Remove-AzVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="04d20-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="04d20-107">EXAMPLES</span></span>

### <span data-ttu-id="04d20-108">Przykład 1: Usuwanie rozszerzenia programu SQL Server</span><span class="sxs-lookup"><span data-stu-id="04d20-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="04d20-109">To polecenie usuwa rozszerzenie programu SQL Server z maszyny wirtualnej o nazwie ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="04d20-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="04d20-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="04d20-110">PARAMETERS</span></span>

### <span data-ttu-id="04d20-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04d20-111">-DefaultProfile</span></span>
<span data-ttu-id="04d20-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="04d20-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04d20-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="04d20-113">-Name</span></span>
<span data-ttu-id="04d20-114">Określa nazwę rozszerzenia programu SQL Server, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04d20-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="04d20-115">-Nowait</span><span class="sxs-lookup"><span data-stu-id="04d20-115">-NoWait</span></span>
<span data-ttu-id="04d20-116">Rozpoczyna operację i wraca natychmiast, zanim operacja zostanie ukończona.</span><span class="sxs-lookup"><span data-stu-id="04d20-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="04d20-117">W celu ustalenia, czy operacja została wykonana pomyślnie, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="04d20-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="04d20-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04d20-118">-ResourceGroupName</span></span>
<span data-ttu-id="04d20-119">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="04d20-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="04d20-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="04d20-120">-VMName</span></span>
<span data-ttu-id="04d20-121">Określa nazwę maszyny wirtualnej, z której to polecenie cmdlet usuwa rozszerzenie programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="04d20-121">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

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

### <span data-ttu-id="04d20-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04d20-122">CommonParameters</span></span>
<span data-ttu-id="04d20-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04d20-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04d20-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="04d20-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04d20-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="04d20-125">INPUTS</span></span>

### <span data-ttu-id="04d20-126">System. String</span><span class="sxs-lookup"><span data-stu-id="04d20-126">System.String</span></span>

## <span data-ttu-id="04d20-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="04d20-127">OUTPUTS</span></span>

### <span data-ttu-id="04d20-128">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="04d20-128">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="04d20-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="04d20-129">NOTES</span></span>

## <span data-ttu-id="04d20-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="04d20-130">RELATED LINKS</span></span>

[<span data-ttu-id="04d20-131">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="04d20-131">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="04d20-132">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="04d20-132">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


