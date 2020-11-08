---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azsqlvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMConfig.md
ms.openlocfilehash: 0f914ab2f5c39cd53239302b2f0acd12a3e13133
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225912"
---
# <span data-ttu-id="18ebb-101">New-AzSqlVMConfig</span><span class="sxs-lookup"><span data-stu-id="18ebb-101">New-AzSqlVMConfig</span></span>

## <span data-ttu-id="18ebb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="18ebb-102">SYNOPSIS</span></span>
<span data-ttu-id="18ebb-103">Tworzy nową konfigurację dla maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="18ebb-103">Creates a new configuration for a sql virtual machine.</span></span>

## <span data-ttu-id="18ebb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="18ebb-104">SYNTAX</span></span>

```
New-AzSqlVMConfig [-LicenseType] <String> [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18ebb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="18ebb-105">DESCRIPTION</span></span>
<span data-ttu-id="18ebb-106">Polecenie cmdlet New-AzSqlVMConfig tworzy nowy obiekt konfiguracji dla maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="18ebb-106">The New-AzSqlVMConfig cmdlet creates a new configuration object for a sql virtual machine.</span></span>

## <span data-ttu-id="18ebb-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="18ebb-107">EXAMPLES</span></span>

### <span data-ttu-id="18ebb-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="18ebb-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzSqlVMConfig -LicenseType "PAYG"
PS C:\> New-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm" -SqlVM $config
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="18ebb-109">Tworzy lokalny obiekt konfigurowalny maszyny wirtualnej SQL, którego można użyć w celu utworzenia maszyny wirtualnej Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="18ebb-109">Creates a local configurable object of sql virtual machine that can be used in order to create an Azure sql virtual machine.</span></span>

## <span data-ttu-id="18ebb-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="18ebb-110">PARAMETERS</span></span>

### <span data-ttu-id="18ebb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18ebb-111">-DefaultProfile</span></span>
<span data-ttu-id="18ebb-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="18ebb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18ebb-113">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="18ebb-113">-LicenseType</span></span>
<span data-ttu-id="18ebb-114">Typ licencji maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="18ebb-114">SQL virtual machine license type.</span></span>

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

### <span data-ttu-id="18ebb-115">-Offer</span><span class="sxs-lookup"><span data-stu-id="18ebb-115">-Offer</span></span>
<span data-ttu-id="18ebb-116">Oferta maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="18ebb-116">SQL virtual machine offer.</span></span>

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

### <span data-ttu-id="18ebb-117">-SKU</span><span class="sxs-lookup"><span data-stu-id="18ebb-117">-Sku</span></span>
<span data-ttu-id="18ebb-118">Typ wydania maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="18ebb-118">SQL virtual machine edition type.</span></span>

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

### <span data-ttu-id="18ebb-119">-Sqlmanagementtype</span><span class="sxs-lookup"><span data-stu-id="18ebb-119">-SqlManagementType</span></span>
<span data-ttu-id="18ebb-120">Typ zarządzania maszyną wirtualną SQL.</span><span class="sxs-lookup"><span data-stu-id="18ebb-120">SQL virtual machine management type.</span></span>

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

### <span data-ttu-id="18ebb-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="18ebb-121">-Tag</span></span>
<span data-ttu-id="18ebb-122">Tagi, które mają zostać skojarzone z maszyną wirtualną SQL</span><span class="sxs-lookup"><span data-stu-id="18ebb-122">The tags to associate with the SQL virtual machine</span></span>

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

### <span data-ttu-id="18ebb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18ebb-123">CommonParameters</span></span>
<span data-ttu-id="18ebb-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18ebb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18ebb-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="18ebb-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18ebb-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="18ebb-126">INPUTS</span></span>

### <span data-ttu-id="18ebb-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="18ebb-127">None</span></span>

## <span data-ttu-id="18ebb-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="18ebb-128">OUTPUTS</span></span>

### <span data-ttu-id="18ebb-129">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="18ebb-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="18ebb-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="18ebb-130">NOTES</span></span>

## <span data-ttu-id="18ebb-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="18ebb-131">RELATED LINKS</span></span>
