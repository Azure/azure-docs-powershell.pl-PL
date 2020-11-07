---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3B15C734-DF57-433A-8854-ACE2B35FF6CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAEMExtension.md
ms.openlocfilehash: deaa8470a4af38eba1f38581e03165c19b3b18f3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706198"
---
# <span data-ttu-id="de536-101">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="de536-101">Set-AzVMAEMExtension</span></span>

## <span data-ttu-id="de536-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="de536-102">SYNOPSIS</span></span>
<span data-ttu-id="de536-103">Włączanie obsługi monitorowania systemów SAP.</span><span class="sxs-lookup"><span data-stu-id="de536-103">Enables support for monitoring for SAP systems.</span></span>

## <span data-ttu-id="de536-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="de536-104">SYNTAX</span></span>

```
Set-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [-EnableWAD]
 [[-WADStorageAccountName] <String>] [[-OSType] <String>] [-SkipStorage] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de536-105">Opis</span><span class="sxs-lookup"><span data-stu-id="de536-105">DESCRIPTION</span></span>
<span data-ttu-id="de536-106">Polecenie cmdlet **Set-AzVMAEMExtension** umożliwia zaktualizowanie konfiguracji maszyny wirtualnej w celu włączenia lub zaktualizowania pomocy technicznej dotyczącej monitorowania systemów SAP zainstalowanych na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="de536-106">The **Set-AzVMAEMExtension** cmdlet updates the configuration of a virtual machine to enable or update the support for monitoring for SAP systems that are installed on the virtual machine.</span></span>
<span data-ttu-id="de536-107">Polecenie cmdlet umożliwia zainstalowanie rozszerzenia rozszerzonego monitorowania platformy Azure (AEM) zbierającego dane dotyczące wydajności i umożliwia odnajdowanie go dla systemu SAP.</span><span class="sxs-lookup"><span data-stu-id="de536-107">The cmdlet installs the Azure Enhanced Monitoring (AEM) extension that collects the performance data and makes it discoverable for the SAP system.</span></span>

## <span data-ttu-id="de536-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="de536-108">EXAMPLES</span></span>

### <span data-ttu-id="de536-109">Przykład 1: Używanie rozszerzenia AEM</span><span class="sxs-lookup"><span data-stu-id="de536-109">Example 1: Use AEM extension</span></span>
```
PS C:\> Set-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server" -WADStorageAccountName "stdstorage"
```

<span data-ttu-id="de536-110">To polecenie umożliwia skonfigurowanie maszyny wirtualnej o nazwie contoso — serwer w celu używania rozszerzenia AEM.</span><span class="sxs-lookup"><span data-stu-id="de536-110">This command configures the virtual machine named contoso-server to use the AEM extension.</span></span>
<span data-ttu-id="de536-111">To polecenie Określa konto magazynu o nazwie stdstorage.</span><span class="sxs-lookup"><span data-stu-id="de536-111">The command specifies the storage account named stdstorage.</span></span>

## <span data-ttu-id="de536-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="de536-112">PARAMETERS</span></span>

### <span data-ttu-id="de536-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de536-113">-DefaultProfile</span></span>
<span data-ttu-id="de536-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="de536-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de536-115">-EnableWAD</span><span class="sxs-lookup"><span data-stu-id="de536-115">-EnableWAD</span></span>
<span data-ttu-id="de536-116">Jeśli ten parametr zostanie podany, unifiedgroup włączy diagnostykę platformy Windows Azure dla tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="de536-116">If this parameter is provided, the commandlet will enable Windows Azure Diagnostics for this virtual machine.</span></span>

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

### <span data-ttu-id="de536-117">-Nowait</span><span class="sxs-lookup"><span data-stu-id="de536-117">-NoWait</span></span>
<span data-ttu-id="de536-118">Rozpoczyna operację i wraca natychmiast, zanim operacja zostanie ukończona.</span><span class="sxs-lookup"><span data-stu-id="de536-118">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="de536-119">W celu ustalenia, czy operacja została wykonana pomyślnie, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="de536-119">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="de536-120">-OSType</span><span class="sxs-lookup"><span data-stu-id="de536-120">-OSType</span></span>
<span data-ttu-id="de536-121">Określa typ systemu operacyjnego dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="de536-121">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="de536-122">Jeśli dysk systemu operacyjnego nie ma typu, należy określić ten parametr.</span><span class="sxs-lookup"><span data-stu-id="de536-122">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="de536-123">Dopuszczalne wartości tego parametru to: Windows i Linux.</span><span class="sxs-lookup"><span data-stu-id="de536-123">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="de536-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de536-124">-ResourceGroupName</span></span>
<span data-ttu-id="de536-125">Określa nazwę grupy zasobów maszyny wirtualnej, którą to polecenie cmdlet modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="de536-125">Specifies the name of the resource group of the virtual machine that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="de536-126">-SkipStorage</span><span class="sxs-lookup"><span data-stu-id="de536-126">-SkipStorage</span></span>
<span data-ttu-id="de536-127">Wskazuje, że to polecenie cmdlet pominie konfigurację miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="de536-127">Indicates that this cmdlet skips configuration of storage.</span></span>

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

### <span data-ttu-id="de536-128">-VMName</span><span class="sxs-lookup"><span data-stu-id="de536-128">-VMName</span></span>
<span data-ttu-id="de536-129">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="de536-129">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="de536-130">To polecenie cmdlet umożliwia dodanie rozszerzenia AEM dla maszyny wirtualnej, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="de536-130">This cmdlet adds the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="de536-131">-WADStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="de536-131">-WADStorageAccountName</span></span>
<span data-ttu-id="de536-132">Określa nazwę konta magazynu, którego używa polecenie cmdlet w celu skonfigurowania rozszerzenia LinuxDiagnostics lub IaaSDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="de536-132">Specifies the name of the storage account that this cmdlet uses to configure the LinuxDiagnostics or IaaSDiagnostics extension.</span></span>
<span data-ttu-id="de536-133">Jeśli maszyna wirtualna nie korzysta ze standardowego konta magazynu, należy określić wartość dla tego parametru.</span><span class="sxs-lookup"><span data-stu-id="de536-133">If the virtual machine does not use a standard storage account, you must specify a value for this parameter.</span></span>

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

### <span data-ttu-id="de536-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de536-134">CommonParameters</span></span>
<span data-ttu-id="de536-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de536-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de536-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="de536-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de536-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="de536-137">INPUTS</span></span>

### <span data-ttu-id="de536-138">System. String</span><span class="sxs-lookup"><span data-stu-id="de536-138">System.String</span></span>

## <span data-ttu-id="de536-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="de536-139">OUTPUTS</span></span>

### <span data-ttu-id="de536-140">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="de536-140">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="de536-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="de536-141">NOTES</span></span>

## <span data-ttu-id="de536-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="de536-142">RELATED LINKS</span></span>

[<span data-ttu-id="de536-143">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="de536-143">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="de536-144">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="de536-144">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="de536-145">Test — AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="de536-145">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)

