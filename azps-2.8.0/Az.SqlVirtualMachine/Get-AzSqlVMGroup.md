---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/get-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVMGroup.md
ms.openlocfilehash: 1d6c7ef54248258fc6a641dc6c917866163bd52a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93887650"
---
# <span data-ttu-id="0f59f-101">Get-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="0f59f-101">Get-AzSqlVMGroup</span></span>

## <span data-ttu-id="0f59f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0f59f-102">SYNOPSIS</span></span>
<span data-ttu-id="0f59f-103">Umożliwia pobieranie jednej lub wielu grup maszyn wirtualnych SQL.</span><span class="sxs-lookup"><span data-stu-id="0f59f-103">Gets one or more sql virtual machine groups.</span></span>

## <span data-ttu-id="0f59f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0f59f-104">SYNTAX</span></span>

### <span data-ttu-id="0f59f-105">ResourceGroupOnly (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0f59f-105">ResourceGroupOnly (Default)</span></span>
```
Get-AzSqlVMGroup [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0f59f-106">Nazwę</span><span class="sxs-lookup"><span data-stu-id="0f59f-106">Name</span></span>
```
Get-AzSqlVMGroup [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0f59f-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="0f59f-107">ResourceId</span></span>
```
Get-AzSqlVMGroup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f59f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="0f59f-108">DESCRIPTION</span></span>
<span data-ttu-id="0f59f-109">Polecenie cmdlet Get-AzSqlVMGroup umożliwia pobieranie jednej lub wielu grup maszyn wirtualnych SQL.</span><span class="sxs-lookup"><span data-stu-id="0f59f-109">The Get-AzSqlVMGroup cmdlet gets one or more sql virtual machine groups.</span></span>

## <span data-ttu-id="0f59f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0f59f-110">EXAMPLES</span></span>

### <span data-ttu-id="0f59f-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0f59f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup

Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
group1     ResourceGroup02    Developer SQL2017-WS2016
```

<span data-ttu-id="0f59f-112">To polecenie pobiera informacje dotyczące wszystkich grup maszyn wirtualnych usługi Azure SQL w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="0f59f-112">This command gets information about all the Azure SQL virtual machine groups in the current subscription.</span></span>

### <span data-ttu-id="0f59f-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="0f59f-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup -ResourceGroupName "ResourceGroup01"
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="0f59f-114">To polecenie pobiera informacje dotyczące wszystkich grup maszyn wirtualnych usługi Azure SQL w bieżącej subskrypcji przypisanych do grupy zasobów ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="0f59f-114">This command gets information about all the Azure SQL virtual machine groups in the current subscription assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="0f59f-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="0f59f-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup -ResourceGroupName "ResourceGroup01" -Name "test-group"
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="0f59f-116">To polecenie pobiera informacje o grupie "test-Grupa maszyny wirtualnej SQL" przypisanej do grupy zasobów ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="0f59f-116">This command gets information about the SQL virtual machine group "test-group" assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="0f59f-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0f59f-117">PARAMETERS</span></span>

### <span data-ttu-id="0f59f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f59f-118">-DefaultProfile</span></span>
<span data-ttu-id="0f59f-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0f59f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f59f-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0f59f-120">-Name</span></span>
<span data-ttu-id="0f59f-121">Nazwa grupy maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="0f59f-121">SQL virtual machine group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: SqlVMGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f59f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f59f-122">-ResourceGroupName</span></span>
<span data-ttu-id="0f59f-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0f59f-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupOnly
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="0f59f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f59f-124">-ResourceId</span></span>
<span data-ttu-id="0f59f-125">Identyfikator zasobu grupy maszyn wirtualnych SQL.</span><span class="sxs-lookup"><span data-stu-id="0f59f-125">SQL virtual machine group resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: SqlVMGroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f59f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f59f-126">CommonParameters</span></span>
<span data-ttu-id="0f59f-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f59f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f59f-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0f59f-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f59f-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0f59f-129">INPUTS</span></span>

### <span data-ttu-id="0f59f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="0f59f-130">System.String</span></span>

## <span data-ttu-id="0f59f-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0f59f-131">OUTPUTS</span></span>

### <span data-ttu-id="0f59f-132">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="0f59f-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="0f59f-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0f59f-133">NOTES</span></span>

## <span data-ttu-id="0f59f-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0f59f-134">RELATED LINKS</span></span>
