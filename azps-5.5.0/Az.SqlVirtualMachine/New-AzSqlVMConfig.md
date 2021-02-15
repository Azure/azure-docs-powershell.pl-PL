---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azsqlvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMConfig.md
ms.openlocfilehash: 0f914ab2f5c39cd53239302b2f0acd12a3e13133
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241907"
---
# <span data-ttu-id="2568b-101">New-AzSqlVMConfig</span><span class="sxs-lookup"><span data-stu-id="2568b-101">New-AzSqlVMConfig</span></span>

## <span data-ttu-id="2568b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2568b-102">SYNOPSIS</span></span>
<span data-ttu-id="2568b-103">Tworzy nową konfigurację dla maszyny wirtualnej sql.</span><span class="sxs-lookup"><span data-stu-id="2568b-103">Creates a new configuration for a sql virtual machine.</span></span>

## <span data-ttu-id="2568b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2568b-104">SYNTAX</span></span>

```
New-AzSqlVMConfig [-LicenseType] <String> [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2568b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2568b-105">DESCRIPTION</span></span>
<span data-ttu-id="2568b-106">Polecenie New-AzSqlVMConfig cmdlet tworzy nowy obiekt konfiguracji dla maszyny wirtualnej sql.</span><span class="sxs-lookup"><span data-stu-id="2568b-106">The New-AzSqlVMConfig cmdlet creates a new configuration object for a sql virtual machine.</span></span>

## <span data-ttu-id="2568b-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2568b-107">EXAMPLES</span></span>

### <span data-ttu-id="2568b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2568b-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzSqlVMConfig -LicenseType "PAYG"
PS C:\> New-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm" -SqlVM $config
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="2568b-109">Tworzy lokalnie konfigurowalny obiekt maszyny wirtualnej sql, który może być używany do tworzenia maszyny wirtualnej języka Azure sql.</span><span class="sxs-lookup"><span data-stu-id="2568b-109">Creates a local configurable object of sql virtual machine that can be used in order to create an Azure sql virtual machine.</span></span>

## <span data-ttu-id="2568b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2568b-110">PARAMETERS</span></span>

### <span data-ttu-id="2568b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2568b-111">-DefaultProfile</span></span>
<span data-ttu-id="2568b-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2568b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2568b-113">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="2568b-113">-LicenseType</span></span>
<span data-ttu-id="2568b-114">Typ licencji na maszynę wirtualną SQL.</span><span class="sxs-lookup"><span data-stu-id="2568b-114">SQL virtual machine license type.</span></span>

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

### <span data-ttu-id="2568b-115">— Oferta</span><span class="sxs-lookup"><span data-stu-id="2568b-115">-Offer</span></span>
<span data-ttu-id="2568b-116">Oferta na maszynę wirtualną SQL.</span><span class="sxs-lookup"><span data-stu-id="2568b-116">SQL virtual machine offer.</span></span>

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

### <span data-ttu-id="2568b-117">- SKU</span><span class="sxs-lookup"><span data-stu-id="2568b-117">-Sku</span></span>
<span data-ttu-id="2568b-118">Typ wersji programu SQL Virtual Machine.</span><span class="sxs-lookup"><span data-stu-id="2568b-118">SQL virtual machine edition type.</span></span>

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

### <span data-ttu-id="2568b-119">-SqlManagementType</span><span class="sxs-lookup"><span data-stu-id="2568b-119">-SqlManagementType</span></span>
<span data-ttu-id="2568b-120">Typ zarządzania maszynami wirtualnymi SQL.</span><span class="sxs-lookup"><span data-stu-id="2568b-120">SQL virtual machine management type.</span></span>

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

### <span data-ttu-id="2568b-121">— Tag</span><span class="sxs-lookup"><span data-stu-id="2568b-121">-Tag</span></span>
<span data-ttu-id="2568b-122">Tagi do skojarzenia z maszyną wirtualną SQL</span><span class="sxs-lookup"><span data-stu-id="2568b-122">The tags to associate with the SQL virtual machine</span></span>

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

### <span data-ttu-id="2568b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2568b-123">CommonParameters</span></span>
<span data-ttu-id="2568b-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2568b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2568b-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2568b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2568b-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2568b-126">INPUTS</span></span>

### <span data-ttu-id="2568b-127">Brak</span><span class="sxs-lookup"><span data-stu-id="2568b-127">None</span></span>

## <span data-ttu-id="2568b-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2568b-128">OUTPUTS</span></span>

### <span data-ttu-id="2568b-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="2568b-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="2568b-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2568b-130">NOTES</span></span>

## <span data-ttu-id="2568b-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2568b-131">RELATED LINKS</span></span>
