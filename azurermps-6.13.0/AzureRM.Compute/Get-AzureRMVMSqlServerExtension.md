---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CAA3E6A9-7E1A-4D57-A269-0B2D3D9C3BEC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRMVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRMVMSqlServerExtension.md
ms.openlocfilehash: e17e8d55ac831fd87e9af9991b4c8ef4d9686dee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541904"
---
# <span data-ttu-id="b797c-101">Get-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="b797c-101">Get-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="b797c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b797c-102">SYNOPSIS</span></span>
<span data-ttu-id="b797c-103">Pobiera ustawienia rozszerzenia programu SQL Server na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b797c-103">Gets the settings for a SQL Server extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b797c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b797c-104">SYNTAX</span></span>

```
Get-AzureRmVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b797c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b797c-105">DESCRIPTION</span></span>
<span data-ttu-id="b797c-106">Polecenie cmdlet **Get-AzureRmVMSqlServerExtension** pobiera ustawienia infrastruktury programu SQL Server jako agenta usługi (IaaS) na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b797c-106">The **Get-AzureRmVMSqlServerExtension** cmdlet gets the settings of the SQL Server infrastructure as a service (IaaS) Agent on a virtual machine.</span></span>

## <span data-ttu-id="b797c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b797c-107">EXAMPLES</span></span>

### <span data-ttu-id="b797c-108">Przykład 1: uzyskiwanie ustawień rozszerzenia serwera SQL na maszynie wirtualnej</span><span class="sxs-lookup"><span data-stu-id="b797c-108">Example 1: Get the settings of a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzureRmVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="b797c-109">To polecenie pobiera ustawienia rozszerzenia programu SQL Server na maszynie wirtualnej o nazwie ContosoVM07.</span><span class="sxs-lookup"><span data-stu-id="b797c-109">This command gets the settings of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

### <span data-ttu-id="b797c-110">Przykład 2: uzyskiwanie ustawień za pomocą rurociągu</span><span class="sxs-lookup"><span data-stu-id="b797c-110">Example 2: Get the settings by using the pipeline</span></span>
```
PS C:\> Get-AzureRmVM -ServiceName "Service08" -Name "ContosoVM22" | Get-AzureRmVMSqlServerExtension
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="b797c-111">To polecenie umożliwia pobieranie maszyny wirtualnej o nazwie ContosoVM22 w Service08 usługi za pomocą polecenia cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="b797c-111">This command gets the virtual machine named ContosoVM22 on the service Service08 by using the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="b797c-112">Polecenie przekazuje wyniki do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="b797c-112">The command passes the results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b797c-113">Bieżące polecenie uzyskuje ustawienia agenta IaaS programu SQL Server na tej maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b797c-113">The current command gets the settings of the SQL Server IaaS Agent on that virtual machine.</span></span>

### <span data-ttu-id="b797c-114">Przykład 3: uzyskiwanie ustawień konkretnej wersji programu SQL Server</span><span class="sxs-lookup"><span data-stu-id="b797c-114">Example 3: Get the settings of specific SQL Server version</span></span>
```
PS C:\> Get-AzureRmVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07" -Version "1.0"
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="b797c-115">To polecenie uzyskuje ustawienia w wersji 1,0 rozszerzenia SQL Server na maszynie wirtualnej o nazwie ContosoVM07.</span><span class="sxs-lookup"><span data-stu-id="b797c-115">This command gets the settings of version 1.0 of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

## <span data-ttu-id="b797c-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b797c-116">PARAMETERS</span></span>

### <span data-ttu-id="b797c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b797c-117">-DefaultProfile</span></span>
<span data-ttu-id="b797c-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b797c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b797c-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b797c-119">-Name</span></span>
<span data-ttu-id="b797c-120">Określa nazwę rozszerzenia programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b797c-120">Specifies the name of the SQL Server the extension.</span></span>

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

### <span data-ttu-id="b797c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b797c-121">-ResourceGroupName</span></span>
<span data-ttu-id="b797c-122">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b797c-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="b797c-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="b797c-123">-VMName</span></span>
<span data-ttu-id="b797c-124">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b797c-124">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="b797c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b797c-125">CommonParameters</span></span>
<span data-ttu-id="b797c-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b797c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b797c-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b797c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b797c-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b797c-128">INPUTS</span></span>

### <span data-ttu-id="b797c-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b797c-129">System.String</span></span>

## <span data-ttu-id="b797c-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b797c-130">OUTPUTS</span></span>

### <span data-ttu-id="b797c-131">Microsoft. Azure. Commands. COMPUTE. VirtualMachineSqlServerExtensionContext</span><span class="sxs-lookup"><span data-stu-id="b797c-131">Microsoft.Azure.Commands.Compute.VirtualMachineSqlServerExtensionContext</span></span>

## <span data-ttu-id="b797c-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b797c-132">NOTES</span></span>

## <span data-ttu-id="b797c-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b797c-133">RELATED LINKS</span></span>

[<span data-ttu-id="b797c-134">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b797c-134">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="b797c-135">Remove-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="b797c-135">Remove-AzureRmVMSqlServerExtension</span></span>](./Remove-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="b797c-136">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="b797c-136">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


