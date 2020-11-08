---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3B15C734-DF57-433A-8854-ACE2B35FF6CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAEMExtension.md
ms.openlocfilehash: b476254d5b9236aa95a30832499aca65a8a110c0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050405"
---
# <span data-ttu-id="9d7fd-101">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="9d7fd-101">Set-AzVMAEMExtension</span></span>

## <span data-ttu-id="9d7fd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9d7fd-102">SYNOPSIS</span></span>
<span data-ttu-id="9d7fd-103">Włączanie obsługi monitorowania systemów SAP.</span><span class="sxs-lookup"><span data-stu-id="9d7fd-103">Enables support for monitoring for SAP systems.</span></span>

## <span data-ttu-id="9d7fd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9d7fd-104">SYNTAX</span></span>

```
Set-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [-EnableWAD]
 [[-WADStorageAccountName] <String>] [[-OSType] <String>] [-SkipStorage] [-NoWait]
 [-SetAccessToIndividualResources] [-InstallNewExtension] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9d7fd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9d7fd-105">DESCRIPTION</span></span>
<span data-ttu-id="9d7fd-106">Polecenie cmdlet **Set-AzVMAEMExtension** umożliwia zaktualizowanie konfiguracji maszyny wirtualnej w celu włączenia lub zaktualizowania pomocy technicznej dotyczącej monitorowania systemów SAP zainstalowanych na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9d7fd-106">The **Set-AzVMAEMExtension** cmdlet updates the configuration of a virtual machine to enable or update the support for monitoring for SAP systems that are installed on the virtual machine.</span></span>
<span data-ttu-id="9d7fd-107">Polecenie cmdlet umożliwia zainstalowanie rozszerzenia rozszerzonego monitorowania platformy Azure (AEM) zbierającego dane dotyczące wydajności i umożliwia odnajdowanie go dla systemu SAP.</span><span class="sxs-lookup"><span data-stu-id="9d7fd-107">The cmdlet installs the Azure Enhanced Monitoring (AEM) extension that collects the performance data and makes it discoverable for the SAP system.</span></span>

## <span data-ttu-id="9d7fd-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9d7fd-108">EXAMPLES</span></span>

### <span data-ttu-id="9d7fd-109">Przykład 1: Używanie rozszerzenia AEM</span><span class="sxs-lookup"><span data-stu-id="9d7fd-109">Example 1: Use AEM extension</span></span>
```
PS C:\> Set-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server" -WADStorageAccountName "stdstorage"
```

<span data-ttu-id="9d7fd-110">To polecenie umożliwia skonfigurowanie maszyny wirtualnej o nazwie contoso — serwer w celu używania rozszerzenia AEM.</span><span class="sxs-lookup"><span data-stu-id="9d7fd-110">This command configures the virtual machine named contoso-server to use the AEM extension.</span></span>
<span data-ttu-id="9d7fd-111">To polecenie Określa konto magazynu o nazwie stdstorage.</span><span class="sxs-lookup"><span data-stu-id="9d7fd-111">The command specifies the storage account named stdstorage.</span></span>

## <span data-ttu-id="9d7fd-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9d7fd-112">PARAMETERS</span></span>

### <span data-ttu-id="9d7fd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d7fd-113">-DefaultProfile</span></span>
<span data-ttu-id="9d7fd-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9d7fd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d7fd-115">-EnableWAD</span><span class="sxs-lookup"><span data-stu-id="9d7fd-115">-EnableWAD</span></span>
<span data-ttu-id="9d7fd-116">Jeśli ten parametr zostanie podany, unifiedgroup włączy diagnostykę platformy Windows Azure dla tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9d7fd-116">If this parameter is provided, the commandlet will enable Windows Azure Diagnostics for this virtual machine.</span></span>

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

### <span data-ttu-id="9d7fd-117">-InstallNewExtension</span><span class="sxs-lookup"><span data-stu-id="9d7fd-117">-InstallNewExtension</span></span>
<span data-ttu-id="9d7fd-118">Zainstaluj nowe rozszerzenie maszyny wirtualnej dla systemu SAP.</span><span class="sxs-lookup"><span data-stu-id="9d7fd-118">Install the new VM Extension for SAP.</span></span>

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

### <span data-ttu-id="9d7fd-119">-Nowait</span><span class="sxs-lookup"><span data-stu-id="9d7fd-119">-NoWait</span></span>
<span data-ttu-id="9d7fd-120">Rozpoczyna operację i wraca natychmiast, zanim operacja zostanie ukończona.</span><span class="sxs-lookup"><span data-stu-id="9d7fd-120">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="9d7fd-121">W celu ustalenia, czy operacja została wykonana pomyślnie, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="9d7fd-121">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="9d7fd-122">-OSType</span><span class="sxs-lookup"><span data-stu-id="9d7fd-122">-OSType</span></span>
<span data-ttu-id="9d7fd-123">Określa typ systemu operacyjnego dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="9d7fd-123">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="9d7fd-124">Jeśli dysk systemu operacyjnego nie ma typu, należy określić ten parametr.</span><span class="sxs-lookup"><span data-stu-id="9d7fd-124">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="9d7fd-125">Dopuszczalne wartości tego parametru to: Windows i Linux.</span><span class="sxs-lookup"><span data-stu-id="9d7fd-125">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="9d7fd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d7fd-126">-ResourceGroupName</span></span>
<span data-ttu-id="9d7fd-127">Określa nazwę grupy zasobów maszyny wirtualnej, którą to polecenie cmdlet modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="9d7fd-127">Specifies the name of the resource group of the virtual machine that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="9d7fd-128">-SetAccessToIndividualResources</span><span class="sxs-lookup"><span data-stu-id="9d7fd-128">-SetAccessToIndividualResources</span></span>
<span data-ttu-id="9d7fd-129">Ustawia dostęp do tożsamości maszyny wirtualnej na poszczególne zasoby, na przykład dyski danych, a nie całą grupę zasobów.</span><span class="sxs-lookup"><span data-stu-id="9d7fd-129">Sets the access of the VM identity to the individual resources, e.g. data disks instead of the complete resource group.</span></span>

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

### <span data-ttu-id="9d7fd-130">-SkipStorage</span><span class="sxs-lookup"><span data-stu-id="9d7fd-130">-SkipStorage</span></span>
<span data-ttu-id="9d7fd-131">Wskazuje, że to polecenie cmdlet pominie konfigurację miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="9d7fd-131">Indicates that this cmdlet skips configuration of storage.</span></span>

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

### <span data-ttu-id="9d7fd-132">-VMName</span><span class="sxs-lookup"><span data-stu-id="9d7fd-132">-VMName</span></span>
<span data-ttu-id="9d7fd-133">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9d7fd-133">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="9d7fd-134">To polecenie cmdlet umożliwia dodanie rozszerzenia AEM dla maszyny wirtualnej, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="9d7fd-134">This cmdlet adds the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="9d7fd-135">-WADStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9d7fd-135">-WADStorageAccountName</span></span>
<span data-ttu-id="9d7fd-136">Określa nazwę konta magazynu, którego używa polecenie cmdlet w celu skonfigurowania rozszerzenia LinuxDiagnostics lub IaaSDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="9d7fd-136">Specifies the name of the storage account that this cmdlet uses to configure the LinuxDiagnostics or IaaSDiagnostics extension.</span></span>
<span data-ttu-id="9d7fd-137">Jeśli maszyna wirtualna nie korzysta ze standardowego konta magazynu, należy określić wartość dla tego parametru.</span><span class="sxs-lookup"><span data-stu-id="9d7fd-137">If the virtual machine does not use a standard storage account, you must specify a value for this parameter.</span></span>

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

### <span data-ttu-id="9d7fd-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d7fd-138">CommonParameters</span></span>
<span data-ttu-id="9d7fd-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d7fd-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d7fd-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9d7fd-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d7fd-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9d7fd-141">INPUTS</span></span>

### <span data-ttu-id="9d7fd-142">System. String</span><span class="sxs-lookup"><span data-stu-id="9d7fd-142">System.String</span></span>

## <span data-ttu-id="9d7fd-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9d7fd-143">OUTPUTS</span></span>

### <span data-ttu-id="9d7fd-144">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9d7fd-144">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="9d7fd-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9d7fd-145">NOTES</span></span>

## <span data-ttu-id="9d7fd-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9d7fd-146">RELATED LINKS</span></span>

[<span data-ttu-id="9d7fd-147">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="9d7fd-147">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="9d7fd-148">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="9d7fd-148">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="9d7fd-149">Test — AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="9d7fd-149">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


