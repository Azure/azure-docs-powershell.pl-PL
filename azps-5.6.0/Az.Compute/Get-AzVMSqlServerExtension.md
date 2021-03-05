---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CAA3E6A9-7E1A-4D57-A269-0B2D3D9C3BEC
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSqlServerExtension.md
ms.openlocfilehash: e8b09473cc08f7e419488112d5cabb788e622726
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980913"
---
# <span data-ttu-id="7a96c-101">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="7a96c-101">Get-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="7a96c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a96c-102">SYNOPSIS</span></span>
<span data-ttu-id="7a96c-103">Pobiera ustawienia rozszerzenia programu SQL Server na komputerze wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="7a96c-103">Gets the settings for a SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="7a96c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7a96c-104">SYNTAX</span></span>

```
Get-AzVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a96c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="7a96c-105">DESCRIPTION</span></span>
<span data-ttu-id="7a96c-106">Polecenie **cmdlet Get-AzVMSqlServerExtension** pobiera ustawienia infrastruktury programu SQL Server jako agenta usługi (IaaS) na maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7a96c-106">The **Get-AzVMSqlServerExtension** cmdlet gets the settings of the SQL Server infrastructure as a service (IaaS) Agent on a virtual machine.</span></span>

## <span data-ttu-id="7a96c-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7a96c-107">EXAMPLES</span></span>

### <span data-ttu-id="7a96c-108">Przykład 1. Uzyskiwanie ustawień rozszerzenia programu SQL Server na komputerze wirtualnym</span><span class="sxs-lookup"><span data-stu-id="7a96c-108">Example 1: Get the settings of a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="7a96c-109">To polecenie pobiera ustawienia rozszerzenia programu SQL Server na komputerze wirtualnym o nazwie ContosoVM07.</span><span class="sxs-lookup"><span data-stu-id="7a96c-109">This command gets the settings of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

### <span data-ttu-id="7a96c-110">Przykład 2. Uzyskiwanie ustawień przy użyciu potoku</span><span class="sxs-lookup"><span data-stu-id="7a96c-110">Example 2: Get the settings by using the pipeline</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service08" -Name "ContosoVM22" | Get-AzVMSqlServerExtension
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="7a96c-111">To polecenie pobiera maszynę wirtualną o nazwie ContosoVM22 w usłudze Service08 przy użyciu Get-AzVM cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a96c-111">This command gets the virtual machine named ContosoVM22 on the service Service08 by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="7a96c-112">Polecenie przekazuje wyniki do bieżącego polecenia cmdlet przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="7a96c-112">The command passes the results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7a96c-113">Bieżące polecenie pobiera ustawienia agenta IaaS programu SQL Server na tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7a96c-113">The current command gets the settings of the SQL Server IaaS Agent on that virtual machine.</span></span>

### <span data-ttu-id="7a96c-114">Przykład 3. Uzyskiwanie ustawień konkretnej wersji programu SQL Server</span><span class="sxs-lookup"><span data-stu-id="7a96c-114">Example 3: Get the settings of specific SQL Server version</span></span>
```
PS C:\> Get-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07" -Version "1.0"
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="7a96c-115">To polecenie pobiera ustawienia wersji 1.0 rozszerzenia programu SQL Server na komputerze wirtualnym o nazwie ContosoVM07.</span><span class="sxs-lookup"><span data-stu-id="7a96c-115">This command gets the settings of version 1.0 of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

## <span data-ttu-id="7a96c-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a96c-116">PARAMETERS</span></span>

### <span data-ttu-id="7a96c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a96c-117">-DefaultProfile</span></span>
<span data-ttu-id="7a96c-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7a96c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a96c-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7a96c-119">-Name</span></span>
<span data-ttu-id="7a96c-120">Określa nazwę rozszerzenia programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="7a96c-120">Specifies the name of the SQL Server the extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a96c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a96c-121">-ResourceGroupName</span></span>
<span data-ttu-id="7a96c-122">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7a96c-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="7a96c-123">-NAZWA.MASZYNY.WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="7a96c-123">-VMName</span></span>
<span data-ttu-id="7a96c-124">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7a96c-124">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a96c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a96c-125">CommonParameters</span></span>
<span data-ttu-id="7a96c-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a96c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a96c-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7a96c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a96c-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7a96c-128">INPUTS</span></span>

### <span data-ttu-id="7a96c-129">System.String</span><span class="sxs-lookup"><span data-stu-id="7a96c-129">System.String</span></span>

## <span data-ttu-id="7a96c-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7a96c-130">OUTPUTS</span></span>

### <span data-ttu-id="7a96c-131">Microsoft.Azure.Commands.Compute.VirtualMachineSqlServerExtensionContext</span><span class="sxs-lookup"><span data-stu-id="7a96c-131">Microsoft.Azure.Commands.Compute.VirtualMachineSqlServerExtensionContext</span></span>

## <span data-ttu-id="7a96c-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7a96c-132">NOTES</span></span>

## <span data-ttu-id="7a96c-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7a96c-133">RELATED LINKS</span></span>

[<span data-ttu-id="7a96c-134">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="7a96c-134">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="7a96c-135">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="7a96c-135">Remove-AzVMSqlServerExtension</span></span>](./Remove-AzVMSqlServerExtension.md)

[<span data-ttu-id="7a96c-136">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="7a96c-136">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


