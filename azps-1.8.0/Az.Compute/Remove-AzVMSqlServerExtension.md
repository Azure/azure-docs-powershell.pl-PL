---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
ms.openlocfilehash: 630df5bbe6677c7019d372a2a6977cc4c724a421
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710240"
---
# <span data-ttu-id="0bea3-101">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="0bea3-101">Remove-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="0bea3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0bea3-102">SYNOPSIS</span></span>
<span data-ttu-id="0bea3-103">Usuwa rozszerzenie programu SQL Server z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0bea3-103">Removes a SQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="0bea3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0bea3-104">SYNTAX</span></span>

```
Remove-AzVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0bea3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0bea3-105">DESCRIPTION</span></span>
<span data-ttu-id="0bea3-106">Polecenie cmdlet **Remove-AzVMSqlServerExtension** usuwa rozszerzenie serwera AzureSQL z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0bea3-106">The **Remove-AzVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="0bea3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0bea3-107">EXAMPLES</span></span>

### <span data-ttu-id="0bea3-108">Przykład 1: Usuwanie rozszerzenia programu SQL Server</span><span class="sxs-lookup"><span data-stu-id="0bea3-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="0bea3-109">To polecenie usuwa rozszerzenie programu SQL Server z maszyny wirtualnej o nazwie ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="0bea3-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="0bea3-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0bea3-110">PARAMETERS</span></span>

### <span data-ttu-id="0bea3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bea3-111">-DefaultProfile</span></span>
<span data-ttu-id="0bea3-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0bea3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0bea3-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0bea3-113">-Name</span></span>
<span data-ttu-id="0bea3-114">Określa nazwę rozszerzenia programu SQL Server, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0bea3-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0bea3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bea3-115">-ResourceGroupName</span></span>
<span data-ttu-id="0bea3-116">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0bea3-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="0bea3-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="0bea3-117">-VMName</span></span>
<span data-ttu-id="0bea3-118">Określa nazwę maszyny wirtualnej, z której to polecenie cmdlet usuwa rozszerzenie programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="0bea3-118">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

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

### <span data-ttu-id="0bea3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bea3-119">CommonParameters</span></span>
<span data-ttu-id="0bea3-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bea3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bea3-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bea3-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bea3-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0bea3-122">INPUTS</span></span>

### <span data-ttu-id="0bea3-123">System. String</span><span class="sxs-lookup"><span data-stu-id="0bea3-123">System.String</span></span>

## <span data-ttu-id="0bea3-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0bea3-124">OUTPUTS</span></span>

### <span data-ttu-id="0bea3-125">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0bea3-125">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="0bea3-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0bea3-126">NOTES</span></span>

## <span data-ttu-id="0bea3-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0bea3-127">RELATED LINKS</span></span>

[<span data-ttu-id="0bea3-128">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="0bea3-128">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="0bea3-129">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="0bea3-129">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


