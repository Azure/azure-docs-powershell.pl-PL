---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: CAA3E6A9-7E1A-4D57-A269-0B2D3D9C3BEC
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMSqlServerExtension.md
ms.openlocfilehash: a3570a65e5c4f6aa305c4123188d094d9bd4545c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893718"
---
# <span data-ttu-id="ad08c-101">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="ad08c-101">Get-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="ad08c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ad08c-102">SYNOPSIS</span></span>
<span data-ttu-id="ad08c-103">Pobiera ustawienia rozszerzenia programu SQL Server na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ad08c-103">Gets the settings for a SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="ad08c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ad08c-104">SYNTAX</span></span>

```
Get-AzVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad08c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ad08c-105">DESCRIPTION</span></span>
<span data-ttu-id="ad08c-106">Polecenie cmdlet **Get-AzVMSqlServerExtension** pobiera ustawienia infrastruktury programu SQL Server jako agenta usługi (IaaS) na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ad08c-106">The **Get-AzVMSqlServerExtension** cmdlet gets the settings of the SQL Server infrastructure as a service (IaaS) Agent on a virtual machine.</span></span>

## <span data-ttu-id="ad08c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ad08c-107">EXAMPLES</span></span>

### <span data-ttu-id="ad08c-108">Przykład 1: uzyskiwanie ustawień rozszerzenia serwera SQL na maszynie wirtualnej</span><span class="sxs-lookup"><span data-stu-id="ad08c-108">Example 1: Get the settings of a SQL Server extension on a virtual machine</span></span>
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

<span data-ttu-id="ad08c-109">To polecenie pobiera ustawienia rozszerzenia programu SQL Server na maszynie wirtualnej o nazwie ContosoVM07.</span><span class="sxs-lookup"><span data-stu-id="ad08c-109">This command gets the settings of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

### <span data-ttu-id="ad08c-110">Przykład 2: uzyskiwanie ustawień za pomocą rurociągu</span><span class="sxs-lookup"><span data-stu-id="ad08c-110">Example 2: Get the settings by using the pipeline</span></span>
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

<span data-ttu-id="ad08c-111">To polecenie umożliwia pobieranie maszyny wirtualnej o nazwie ContosoVM22 w Service08 usługi za pomocą polecenia cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="ad08c-111">This command gets the virtual machine named ContosoVM22 on the service Service08 by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="ad08c-112">Polecenie przekazuje wyniki do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="ad08c-112">The command passes the results to the current cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="ad08c-113">Bieżące polecenie uzyskuje ustawienia agenta IaaS programu SQL Server na tej maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ad08c-113">The current command gets the settings of the SQL Server IaaS Agent on that virtual machine.</span></span>

### <span data-ttu-id="ad08c-114">Przykład 3: uzyskiwanie ustawień konkretnej wersji programu SQL Server</span><span class="sxs-lookup"><span data-stu-id="ad08c-114">Example 3: Get the settings of specific SQL Server version</span></span>
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

<span data-ttu-id="ad08c-115">To polecenie uzyskuje ustawienia w wersji 1,0 rozszerzenia SQL Server na maszynie wirtualnej o nazwie ContosoVM07.</span><span class="sxs-lookup"><span data-stu-id="ad08c-115">This command gets the settings of version 1.0 of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

## <span data-ttu-id="ad08c-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ad08c-116">PARAMETERS</span></span>

### <span data-ttu-id="ad08c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad08c-117">-DefaultProfile</span></span>
<span data-ttu-id="ad08c-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ad08c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad08c-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ad08c-119">-Name</span></span>
<span data-ttu-id="ad08c-120">Określa nazwę rozszerzenia programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ad08c-120">Specifies the name of the SQL Server the extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad08c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad08c-121">-ResourceGroupName</span></span>
<span data-ttu-id="ad08c-122">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ad08c-122">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad08c-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="ad08c-123">-VMName</span></span>
<span data-ttu-id="ad08c-124">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ad08c-124">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad08c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad08c-125">CommonParameters</span></span>
<span data-ttu-id="ad08c-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad08c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad08c-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad08c-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad08c-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad08c-128">INPUTS</span></span>

### <span data-ttu-id="ad08c-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="ad08c-129">None</span></span>
<span data-ttu-id="ad08c-130">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="ad08c-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ad08c-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ad08c-131">OUTPUTS</span></span>

### <span data-ttu-id="ad08c-132">Microsoft. Azure. Commands. COMPUTE. VirtualMachineSqlServerExtensionContext</span><span class="sxs-lookup"><span data-stu-id="ad08c-132">Microsoft.Azure.Commands.Compute.VirtualMachineSqlServerExtensionContext</span></span>

## <span data-ttu-id="ad08c-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ad08c-133">NOTES</span></span>

## <span data-ttu-id="ad08c-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ad08c-134">RELATED LINKS</span></span>

[<span data-ttu-id="ad08c-135">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="ad08c-135">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="ad08c-136">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="ad08c-136">Remove-AzVMSqlServerExtension</span></span>](./Remove-AzVMSqlServerExtension.md)

[<span data-ttu-id="ad08c-137">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="ad08c-137">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


