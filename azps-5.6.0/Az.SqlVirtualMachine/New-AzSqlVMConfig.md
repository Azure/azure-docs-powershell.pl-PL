---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/new-azsqlvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMConfig.md
ms.openlocfilehash: e12f69cbb36c5fabccffc4102723175c9f6b8909
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992167"
---
# <span data-ttu-id="25133-101">New-AzSqlVMConfig</span><span class="sxs-lookup"><span data-stu-id="25133-101">New-AzSqlVMConfig</span></span>

## <span data-ttu-id="25133-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25133-102">SYNOPSIS</span></span>
<span data-ttu-id="25133-103">Tworzy nową konfigurację dla maszyny wirtualnej sql.</span><span class="sxs-lookup"><span data-stu-id="25133-103">Creates a new configuration for a sql virtual machine.</span></span>

## <span data-ttu-id="25133-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="25133-104">SYNTAX</span></span>

```
New-AzSqlVMConfig [-LicenseType] <String> [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25133-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="25133-105">DESCRIPTION</span></span>
<span data-ttu-id="25133-106">Polecenie New-AzSqlVMConfig cmdlet tworzy nowy obiekt konfiguracji dla maszyny wirtualnej sql.</span><span class="sxs-lookup"><span data-stu-id="25133-106">The New-AzSqlVMConfig cmdlet creates a new configuration object for a sql virtual machine.</span></span>

## <span data-ttu-id="25133-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="25133-107">EXAMPLES</span></span>

### <span data-ttu-id="25133-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="25133-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzSqlVMConfig -LicenseType "PAYG"
PS C:\> New-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm" -SqlVM $config
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="25133-109">Tworzy lokalnie konfigurowalny obiekt maszyny wirtualnej sql, który może być używany do tworzenia maszyny wirtualnej języka Azure sql.</span><span class="sxs-lookup"><span data-stu-id="25133-109">Creates a local configurable object of sql virtual machine that can be used in order to create an Azure sql virtual machine.</span></span>

## <span data-ttu-id="25133-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25133-110">PARAMETERS</span></span>

### <span data-ttu-id="25133-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25133-111">-DefaultProfile</span></span>
<span data-ttu-id="25133-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="25133-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25133-113">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="25133-113">-LicenseType</span></span>
<span data-ttu-id="25133-114">Typ licencji na maszynę wirtualną SQL.</span><span class="sxs-lookup"><span data-stu-id="25133-114">SQL virtual machine license type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25133-115">— Oferta</span><span class="sxs-lookup"><span data-stu-id="25133-115">-Offer</span></span>
<span data-ttu-id="25133-116">Oferta na maszynę wirtualną SQL.</span><span class="sxs-lookup"><span data-stu-id="25133-116">SQL virtual machine offer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25133-117">- SKU</span><span class="sxs-lookup"><span data-stu-id="25133-117">-Sku</span></span>
<span data-ttu-id="25133-118">Typ wersji programu SQL Virtual Machine.</span><span class="sxs-lookup"><span data-stu-id="25133-118">SQL virtual machine edition type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25133-119">-SqlManagementType</span><span class="sxs-lookup"><span data-stu-id="25133-119">-SqlManagementType</span></span>
<span data-ttu-id="25133-120">Typ zarządzania maszynami wirtualnymi SQL.</span><span class="sxs-lookup"><span data-stu-id="25133-120">SQL virtual machine management type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25133-121">— Tag</span><span class="sxs-lookup"><span data-stu-id="25133-121">-Tag</span></span>
<span data-ttu-id="25133-122">Tagi do skojarzenia z maszyną wirtualną SQL</span><span class="sxs-lookup"><span data-stu-id="25133-122">The tags to associate with the SQL virtual machine</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25133-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25133-123">CommonParameters</span></span>
<span data-ttu-id="25133-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25133-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25133-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="25133-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25133-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="25133-126">INPUTS</span></span>

### <span data-ttu-id="25133-127">Brak</span><span class="sxs-lookup"><span data-stu-id="25133-127">None</span></span>

## <span data-ttu-id="25133-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="25133-128">OUTPUTS</span></span>

### <span data-ttu-id="25133-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="25133-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="25133-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="25133-130">NOTES</span></span>

## <span data-ttu-id="25133-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="25133-131">RELATED LINKS</span></span>
