---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
ms.openlocfilehash: 599b4817ce9f4f6f1f7a75f5811c5a3122f1bbb7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052627"
---
# <span data-ttu-id="60255-101">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="60255-101">Remove-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="60255-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="60255-102">SYNOPSIS</span></span>
<span data-ttu-id="60255-103">Usuwa rozszerzenie programu SQL Server z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="60255-103">Removes a SQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="60255-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="60255-104">SYNTAX</span></span>

```
Remove-AzVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60255-105">Opis</span><span class="sxs-lookup"><span data-stu-id="60255-105">DESCRIPTION</span></span>
<span data-ttu-id="60255-106">Polecenie cmdlet **Remove-AzVMSqlServerExtension** usuwa rozszerzenie serwera AzureSQL z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="60255-106">The **Remove-AzVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="60255-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="60255-107">EXAMPLES</span></span>

### <span data-ttu-id="60255-108">Przykład 1: Usuwanie rozszerzenia programu SQL Server</span><span class="sxs-lookup"><span data-stu-id="60255-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="60255-109">To polecenie usuwa rozszerzenie programu SQL Server z maszyny wirtualnej o nazwie ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="60255-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="60255-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="60255-110">PARAMETERS</span></span>

### <span data-ttu-id="60255-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60255-111">-DefaultProfile</span></span>
<span data-ttu-id="60255-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="60255-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60255-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="60255-113">-Name</span></span>
<span data-ttu-id="60255-114">Określa nazwę rozszerzenia programu SQL Server, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60255-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="60255-115">-Nowait</span><span class="sxs-lookup"><span data-stu-id="60255-115">-NoWait</span></span>
<span data-ttu-id="60255-116">Rozpoczyna operację i wraca natychmiast, zanim operacja zostanie ukończona.</span><span class="sxs-lookup"><span data-stu-id="60255-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="60255-117">W celu ustalenia, czy operacja została wykonana pomyślnie, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="60255-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="60255-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60255-118">-ResourceGroupName</span></span>
<span data-ttu-id="60255-119">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="60255-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="60255-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="60255-120">-VMName</span></span>
<span data-ttu-id="60255-121">Określa nazwę maszyny wirtualnej, z której to polecenie cmdlet usuwa rozszerzenie programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="60255-121">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

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

### <span data-ttu-id="60255-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60255-122">CommonParameters</span></span>
<span data-ttu-id="60255-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60255-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60255-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="60255-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60255-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="60255-125">INPUTS</span></span>

### <span data-ttu-id="60255-126">System. String</span><span class="sxs-lookup"><span data-stu-id="60255-126">System.String</span></span>

## <span data-ttu-id="60255-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="60255-127">OUTPUTS</span></span>

### <span data-ttu-id="60255-128">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="60255-128">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="60255-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="60255-129">NOTES</span></span>

## <span data-ttu-id="60255-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="60255-130">RELATED LINKS</span></span>

[<span data-ttu-id="60255-131">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="60255-131">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="60255-132">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="60255-132">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


