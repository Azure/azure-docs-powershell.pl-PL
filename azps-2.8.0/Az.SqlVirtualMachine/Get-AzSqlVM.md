---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/get-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVM.md
ms.openlocfilehash: 6d525d09c181f71a1b4740932179581a03235afe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93887649"
---
# <span data-ttu-id="da9da-101">Get-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="da9da-101">Get-AzSqlVM</span></span>

## <span data-ttu-id="da9da-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="da9da-102">SYNOPSIS</span></span>
<span data-ttu-id="da9da-103">Pobiera co najmniej jeden wirtualny maszynę SQL.</span><span class="sxs-lookup"><span data-stu-id="da9da-103">Gets one or more sql virtual machines.</span></span>

## <span data-ttu-id="da9da-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="da9da-104">SYNTAX</span></span>

### <span data-ttu-id="da9da-105">ResourceGroupOnly (domyślny)</span><span class="sxs-lookup"><span data-stu-id="da9da-105">ResourceGroupOnly (Default)</span></span>
```
Get-AzSqlVM [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da9da-106">Nazwę</span><span class="sxs-lookup"><span data-stu-id="da9da-106">Name</span></span>
```
Get-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="da9da-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="da9da-107">ResourceId</span></span>
```
Get-AzSqlVM [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da9da-108">Opis</span><span class="sxs-lookup"><span data-stu-id="da9da-108">DESCRIPTION</span></span>
<span data-ttu-id="da9da-109">Polecenie cmdlet Get-AzSqlVM umożliwia pobieranie co najmniej jednej maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="da9da-109">The Get-AzSqlVM cmdlet gets one or more sql virtual machines.</span></span>

## <span data-ttu-id="da9da-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="da9da-110">EXAMPLES</span></span>

### <span data-ttu-id="da9da-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="da9da-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlVM

Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
vm2  ResourceGroup02    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="da9da-112">To polecenie pobiera informacje o wszystkich maszynach wirtualnych usługi Azure SQL w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="da9da-112">This command gets information about all the Azure SQL virtual machines in the current subscription.</span></span>

### <span data-ttu-id="da9da-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="da9da-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlVM -ResourceGroupName "ResourceGroup01"
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="da9da-114">To polecenie pobiera informacje o wszystkich maszynach wirtualnych SQL Azure w bieżącej subskrypcji przypisanych do grupy zasobów ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="da9da-114">This command gets information about all the Azure SQL virtual machines in the current subscription assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="da9da-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="da9da-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm"
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="da9da-116">To polecenie pobiera informacje o maszynie wirtualnej SQL "VM" przypisanej do grupy zasobów ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="da9da-116">This command gets information about the SQL virtual machine "vm" assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="da9da-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="da9da-117">PARAMETERS</span></span>

### <span data-ttu-id="da9da-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da9da-118">-DefaultProfile</span></span>
<span data-ttu-id="da9da-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="da9da-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da9da-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="da9da-120">-Name</span></span>
<span data-ttu-id="da9da-121">Nazwa maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="da9da-121">SQL virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: SqlVMName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da9da-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da9da-122">-ResourceGroupName</span></span>
<span data-ttu-id="da9da-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="da9da-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="da9da-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="da9da-124">-ResourceId</span></span>
<span data-ttu-id="da9da-125">Identyfikator zasobu maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="da9da-125">SQL virtual machine resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: SqlVMId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da9da-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da9da-126">CommonParameters</span></span>
<span data-ttu-id="da9da-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da9da-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da9da-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="da9da-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da9da-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="da9da-129">INPUTS</span></span>

### <span data-ttu-id="da9da-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="da9da-130">None</span></span>

## <span data-ttu-id="da9da-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="da9da-131">OUTPUTS</span></span>

### <span data-ttu-id="da9da-132">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="da9da-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="da9da-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="da9da-133">NOTES</span></span>

## <span data-ttu-id="da9da-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="da9da-134">RELATED LINKS</span></span>
