---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3B15C734-DF57-433A-8854-ACE2B35FF6CB
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAEMExtension.md
ms.openlocfilehash: 4784df2e4ab6d24923bb4c7619e18459101bdf41
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004570"
---
# <span data-ttu-id="cdb83-101">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="cdb83-101">Set-AzVMAEMExtension</span></span>

## <span data-ttu-id="cdb83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cdb83-102">SYNOPSIS</span></span>
<span data-ttu-id="cdb83-103">Umożliwia monitorowanie systemów SAP.</span><span class="sxs-lookup"><span data-stu-id="cdb83-103">Enables support for monitoring for SAP systems.</span></span>

## <span data-ttu-id="cdb83-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cdb83-104">SYNTAX</span></span>

```
Set-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [-EnableWAD]
 [[-WADStorageAccountName] <String>] [[-OSType] <String>] [-SkipStorage] [-NoWait]
 [-SetAccessToIndividualResources] [-InstallNewExtension] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cdb83-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="cdb83-105">DESCRIPTION</span></span>
<span data-ttu-id="cdb83-106">Polecenie cmdlet **Set-AzVMAEMExtension** aktualizuje konfigurację maszyny wirtualnej w celu włączenia lub zaktualizowania obsługi monitorowania systemów SAP zainstalowanych na maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="cdb83-106">The **Set-AzVMAEMExtension** cmdlet updates the configuration of a virtual machine to enable or update the support for monitoring for SAP systems that are installed on the virtual machine.</span></span>
<span data-ttu-id="cdb83-107">Polecenie cmdlet instaluje rozszerzenie Azure Enhanced Monitoring (AEM), które zbiera dane dotyczące wydajności i umożliwia jego wykrywanie dla systemu SAP.</span><span class="sxs-lookup"><span data-stu-id="cdb83-107">The cmdlet installs the Azure Enhanced Monitoring (AEM) extension that collects the performance data and makes it discoverable for the SAP system.</span></span>

## <span data-ttu-id="cdb83-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cdb83-108">EXAMPLES</span></span>

### <span data-ttu-id="cdb83-109">Przykład 1. Używanie rozszerzenia AEM</span><span class="sxs-lookup"><span data-stu-id="cdb83-109">Example 1: Use AEM extension</span></span>
```
PS C:\> Set-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server" -WADStorageAccountName "stdstorage"
```

<span data-ttu-id="cdb83-110">To polecenie konfiguruje maszynę wirtualną o nazwie contoso-server do używania rozszerzenia AEM.</span><span class="sxs-lookup"><span data-stu-id="cdb83-110">This command configures the virtual machine named contoso-server to use the AEM extension.</span></span>
<span data-ttu-id="cdb83-111">To polecenie określa konto magazynu o nazwie stdstorage.</span><span class="sxs-lookup"><span data-stu-id="cdb83-111">The command specifies the storage account named stdstorage.</span></span>

## <span data-ttu-id="cdb83-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cdb83-112">PARAMETERS</span></span>

### <span data-ttu-id="cdb83-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdb83-113">-DefaultProfile</span></span>
<span data-ttu-id="cdb83-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cdb83-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cdb83-115">- EnableWAD</span><span class="sxs-lookup"><span data-stu-id="cdb83-115">-EnableWAD</span></span>
<span data-ttu-id="cdb83-116">Jeśli ten parametr jest podany, polecenie commandlet włączy usługę Windows Azure Diagnostics dla tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="cdb83-116">If this parameter is provided, the commandlet will enable Windows Azure Diagnostics for this virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdb83-117">-InstallNewExtension</span><span class="sxs-lookup"><span data-stu-id="cdb83-117">-InstallNewExtension</span></span>
<span data-ttu-id="cdb83-118">Zainstaluj nowe rozszerzenie maszyny wirtualnej dla systemu SAP.</span><span class="sxs-lookup"><span data-stu-id="cdb83-118">Install the new VM Extension for SAP.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdb83-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="cdb83-119">-NoWait</span></span>
<span data-ttu-id="cdb83-120">Rozpoczyna operację i zwraca bezpośrednio przed jej ukończeniem.</span><span class="sxs-lookup"><span data-stu-id="cdb83-120">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="cdb83-121">Aby ustalić, czy operacja została pomyślnie ukończona, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="cdb83-121">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="cdb83-122">- OSType</span><span class="sxs-lookup"><span data-stu-id="cdb83-122">-OSType</span></span>
<span data-ttu-id="cdb83-123">Określa typ systemu operacyjnego dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="cdb83-123">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="cdb83-124">Jeśli dysk systemu operacyjnego nie ma typu, musisz określić ten parametr.</span><span class="sxs-lookup"><span data-stu-id="cdb83-124">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="cdb83-125">Dopuszczalne wartości dla tego parametru to: Windows i Linux.</span><span class="sxs-lookup"><span data-stu-id="cdb83-125">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdb83-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdb83-126">-ResourceGroupName</span></span>
<span data-ttu-id="cdb83-127">Określa nazwę grupy zasobów maszyny wirtualnej, która ma być zmieniana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cdb83-127">Specifies the name of the resource group of the virtual machine that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="cdb83-128">-SetAccessToIndividualResources</span><span class="sxs-lookup"><span data-stu-id="cdb83-128">-SetAccessToIndividualResources</span></span>
<span data-ttu-id="cdb83-129">Ustawia dostęp tożsamości maszyny WIRTUALNEj do poszczególnych zasobów, na przykład do dyskietek danych zamiast do pełnej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cdb83-129">Sets the access of the VM identity to the individual resources, e.g. data disks instead of the complete resource group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdb83-130">- SkipStorage</span><span class="sxs-lookup"><span data-stu-id="cdb83-130">-SkipStorage</span></span>
<span data-ttu-id="cdb83-131">Wskazuje, że to polecenie cmdlet pomija konfigurację magazynu.</span><span class="sxs-lookup"><span data-stu-id="cdb83-131">Indicates that this cmdlet skips configuration of storage.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdb83-132">-NAZWA.MASZYNY.WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="cdb83-132">-VMName</span></span>
<span data-ttu-id="cdb83-133">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="cdb83-133">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="cdb83-134">To polecenie cmdlet dodaje rozszerzenie AEM dla maszyny wirtualnej, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="cdb83-134">This cmdlet adds the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="cdb83-135">-WADStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="cdb83-135">-WADStorageAccountName</span></span>
<span data-ttu-id="cdb83-136">Określa nazwę konta magazynu używanego przez to polecenie cmdlet do konfigurowania rozszerzenia LinuxDiagnostics lub IaaSDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="cdb83-136">Specifies the name of the storage account that this cmdlet uses to configure the LinuxDiagnostics or IaaSDiagnostics extension.</span></span>
<span data-ttu-id="cdb83-137">Jeśli maszyny wirtualnej nie używa standardowego konta magazynu, należy określić wartość dla tego parametru.</span><span class="sxs-lookup"><span data-stu-id="cdb83-137">If the virtual machine does not use a standard storage account, you must specify a value for this parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdb83-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdb83-138">CommonParameters</span></span>
<span data-ttu-id="cdb83-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdb83-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdb83-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cdb83-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdb83-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cdb83-141">INPUTS</span></span>

### <span data-ttu-id="cdb83-142">System.String</span><span class="sxs-lookup"><span data-stu-id="cdb83-142">System.String</span></span>

## <span data-ttu-id="cdb83-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cdb83-143">OUTPUTS</span></span>

### <span data-ttu-id="cdb83-144">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="cdb83-144">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="cdb83-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cdb83-145">NOTES</span></span>

## <span data-ttu-id="cdb83-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cdb83-146">RELATED LINKS</span></span>

[<span data-ttu-id="cdb83-147">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="cdb83-147">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="cdb83-148">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="cdb83-148">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="cdb83-149">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="cdb83-149">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


