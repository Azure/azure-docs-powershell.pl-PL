---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3B15C734-DF57-433A-8854-ACE2B35FF6CB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMAEMExtension.md
ms.openlocfilehash: 931ed484850654ecebc368ced0b378ce2a40944f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525594"
---
# <span data-ttu-id="1d39b-101">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="1d39b-101">Set-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="1d39b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1d39b-102">SYNOPSIS</span></span>
<span data-ttu-id="1d39b-103">Włączanie obsługi monitorowania systemów SAP.</span><span class="sxs-lookup"><span data-stu-id="1d39b-103">Enables support for monitoring for SAP systems.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d39b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1d39b-104">SYNTAX</span></span>

```
Set-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [-DisableWAD] [-EnableWAD]
 [[-WADStorageAccountName] <String>] [[-OSType] <String>] [-SkipStorage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d39b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1d39b-105">DESCRIPTION</span></span>
<span data-ttu-id="1d39b-106">Polecenie cmdlet **Set-AzureRmVMAEMExtension** umożliwia zaktualizowanie konfiguracji maszyny wirtualnej w celu włączenia lub zaktualizowania pomocy technicznej dotyczącej monitorowania systemów SAP zainstalowanych na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1d39b-106">The **Set-AzureRmVMAEMExtension** cmdlet updates the configuration of a virtual machine to enable or update the support for monitoring for SAP systems that are installed on the virtual machine.</span></span>
<span data-ttu-id="1d39b-107">Polecenie cmdlet umożliwia zainstalowanie rozszerzenia rozszerzonego monitorowania platformy Azure (AEM) zbierającego dane dotyczące wydajności i umożliwia odnajdowanie go dla systemu SAP.</span><span class="sxs-lookup"><span data-stu-id="1d39b-107">The cmdlet installs the Azure Enhanced Monitoring (AEM) extension that collects the performance data and makes it discoverable for the SAP system.</span></span>

## <span data-ttu-id="1d39b-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1d39b-108">EXAMPLES</span></span>

### <span data-ttu-id="1d39b-109">Przykład 1: Używanie rozszerzenia AEM</span><span class="sxs-lookup"><span data-stu-id="1d39b-109">Example 1: Use AEM extension</span></span>
```
PS C:\> Set-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server" -WADStorageAccountName "stdstorage"
```

<span data-ttu-id="1d39b-110">To polecenie umożliwia skonfigurowanie maszyny wirtualnej o nazwie contoso — serwer w celu używania rozszerzenia AEM.</span><span class="sxs-lookup"><span data-stu-id="1d39b-110">This command configures the virtual machine named contoso-server to use the AEM extension.</span></span>
<span data-ttu-id="1d39b-111">To polecenie Określa konto magazynu o nazwie stdstorage.</span><span class="sxs-lookup"><span data-stu-id="1d39b-111">The command specifies the storage account named stdstorage.</span></span>

## <span data-ttu-id="1d39b-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1d39b-112">PARAMETERS</span></span>

### <span data-ttu-id="1d39b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d39b-113">-DefaultProfile</span></span>
<span data-ttu-id="1d39b-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1d39b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d39b-115">-DisableWAD</span><span class="sxs-lookup"><span data-stu-id="1d39b-115">-DisableWAD</span></span>
<span data-ttu-id="1d39b-116">Wskazuje, że to polecenie cmdlet nie włącza diagnostyki platformy Azure dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1d39b-116">Indicates that this cmdlet does not enable Azure Diagnostics for the virtual machine.</span></span>

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

### <span data-ttu-id="1d39b-117">-EnableWAD</span><span class="sxs-lookup"><span data-stu-id="1d39b-117">-EnableWAD</span></span>
<span data-ttu-id="1d39b-118">Jeśli ten parametr zostanie podany, unifiedgroup włączy diagnostykę platformy Windows Azure dla tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1d39b-118">If this parameter is provided, the commandlet will enable Windows Azure Diagnostics for this virtual machine.</span></span>

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

### <span data-ttu-id="1d39b-119">-OSType</span><span class="sxs-lookup"><span data-stu-id="1d39b-119">-OSType</span></span>
<span data-ttu-id="1d39b-120">Określa typ systemu operacyjnego dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="1d39b-120">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="1d39b-121">Jeśli dysk systemu operacyjnego nie ma typu, należy określić ten parametr.</span><span class="sxs-lookup"><span data-stu-id="1d39b-121">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="1d39b-122">Dopuszczalne wartości tego parametru to: Windows i Linux.</span><span class="sxs-lookup"><span data-stu-id="1d39b-122">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="1d39b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d39b-123">-ResourceGroupName</span></span>
<span data-ttu-id="1d39b-124">Określa nazwę grupy zasobów maszyny wirtualnej, którą to polecenie cmdlet modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="1d39b-124">Specifies the name of the resource group of the virtual machine that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="1d39b-125">-SkipStorage</span><span class="sxs-lookup"><span data-stu-id="1d39b-125">-SkipStorage</span></span>
<span data-ttu-id="1d39b-126">Wskazuje, że to polecenie cmdlet pominie konfigurację miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="1d39b-126">Indicates that this cmdlet skips configuration of storage.</span></span>

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

### <span data-ttu-id="1d39b-127">-VMName</span><span class="sxs-lookup"><span data-stu-id="1d39b-127">-VMName</span></span>
<span data-ttu-id="1d39b-128">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1d39b-128">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="1d39b-129">To polecenie cmdlet umożliwia dodanie rozszerzenia AEM dla maszyny wirtualnej, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="1d39b-129">This cmdlet adds the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="1d39b-130">-WADStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1d39b-130">-WADStorageAccountName</span></span>
<span data-ttu-id="1d39b-131">Określa nazwę konta magazynu, którego używa polecenie cmdlet w celu skonfigurowania rozszerzenia LinuxDiagnostics lub IaaSDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="1d39b-131">Specifies the name of the storage account that this cmdlet uses to configure the LinuxDiagnostics or IaaSDiagnostics extension.</span></span>
<span data-ttu-id="1d39b-132">Jeśli maszyna wirtualna nie korzysta ze standardowego konta magazynu, należy określić wartość dla tego parametru.</span><span class="sxs-lookup"><span data-stu-id="1d39b-132">If the virtual machine does not use a standard storage account, you must specify a value for this parameter.</span></span>

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

### <span data-ttu-id="1d39b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d39b-133">CommonParameters</span></span>
<span data-ttu-id="1d39b-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d39b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d39b-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d39b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d39b-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1d39b-136">INPUTS</span></span>

## <span data-ttu-id="1d39b-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1d39b-137">OUTPUTS</span></span>

## <span data-ttu-id="1d39b-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1d39b-138">NOTES</span></span>

## <span data-ttu-id="1d39b-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1d39b-139">RELATED LINKS</span></span>

[<span data-ttu-id="1d39b-140">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="1d39b-140">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="1d39b-141">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="1d39b-141">Remove-AzureRmVMAEMExtension</span></span>](./Remove-AzureRmVMAEMExtension.md)

[<span data-ttu-id="1d39b-142">Test — AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="1d39b-142">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)


