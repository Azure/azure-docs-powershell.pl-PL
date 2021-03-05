---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E2A56E55-30A3-4A2F-80AE-9D166840909E
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azremotedesktopfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzRemoteDesktopFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzRemoteDesktopFile.md
ms.openlocfilehash: d06f8b5efa0a220b20c5324b457a870d5aaa44b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981057"
---
# <span data-ttu-id="0e73c-101">Get-AzRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="0e73c-101">Get-AzRemoteDesktopFile</span></span>

## <span data-ttu-id="0e73c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e73c-102">SYNOPSIS</span></span>
<span data-ttu-id="0e73c-103">Pobiera plik rdp.</span><span class="sxs-lookup"><span data-stu-id="0e73c-103">Gets an .rdp file.</span></span>

## <span data-ttu-id="0e73c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0e73c-104">SYNTAX</span></span>

### <span data-ttu-id="0e73c-105">Pobierz</span><span class="sxs-lookup"><span data-stu-id="0e73c-105">Download</span></span>
```
Get-AzRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [-LocalPath] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e73c-106">Uruchom</span><span class="sxs-lookup"><span data-stu-id="0e73c-106">Launch</span></span>
```
Get-AzRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [[-LocalPath] <String>] [-Launch]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e73c-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="0e73c-107">DESCRIPTION</span></span>
<span data-ttu-id="0e73c-108">Polecenie **cmdlet Get-AzRemoteDesktopFile** pobiera plik protokołu pulpitu zdalnego (rdp).</span><span class="sxs-lookup"><span data-stu-id="0e73c-108">The **Get-AzRemoteDesktopFile** cmdlet gets a Remote Desktop Protocol (.rdp) file.</span></span>

## <span data-ttu-id="0e73c-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0e73c-109">EXAMPLES</span></span>

### <span data-ttu-id="0e73c-110">Przykład 1. Uzyskiwanie pliku pulpitu zdalnego</span><span class="sxs-lookup"><span data-stu-id="0e73c-110">Example 1: Get a Remote Desktop file</span></span>
```
PS C:\> Get-AzRemoteDesktopFile -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -LocalPath "D:\RemoteDesktopFile07.rdp"
```

<span data-ttu-id="0e73c-111">To polecenie pobiera plik pulpitu zdalnego dla maszyny wirtualnej o nazwie VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="0e73c-111">This command gets the Remote Desktop file for the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="0e73c-112">Polecenie zapisuje wynik w pliku o nazwie D:\RemoteDesktopFile07.rdp.</span><span class="sxs-lookup"><span data-stu-id="0e73c-112">The command stores the result in the file named D:\RemoteDesktopFile07.rdp.</span></span>

## <span data-ttu-id="0e73c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0e73c-113">PARAMETERS</span></span>

### <span data-ttu-id="0e73c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e73c-114">-DefaultProfile</span></span>
<span data-ttu-id="0e73c-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0e73c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e73c-116">— Launch</span><span class="sxs-lookup"><span data-stu-id="0e73c-116">-Launch</span></span>
<span data-ttu-id="0e73c-117">Wskazuje, że to polecenie cmdlet uruchamia pulpit zdalny po pobieraniu pliku rdp.</span><span class="sxs-lookup"><span data-stu-id="0e73c-117">Indicates that this cmdlet launches Remote Desktop after it gets the .rdp file.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Launch
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e73c-118">— LocalPath</span><span class="sxs-lookup"><span data-stu-id="0e73c-118">-LocalPath</span></span>
<span data-ttu-id="0e73c-119">Określa pełną ścieżkę lokalną, w której to polecenie cmdlet przechowuje plik rdp.</span><span class="sxs-lookup"><span data-stu-id="0e73c-119">Specifies the local full path where this cmdlet stores the .rdp file.</span></span>

```yaml
Type: System.String
Parameter Sets: Download
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Launch
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e73c-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0e73c-120">-Name</span></span>
<span data-ttu-id="0e73c-121">Określa nazwę zestawu dostępności, który otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e73c-121">Specifies the name of the availability set that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e73c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e73c-122">-ResourceGroupName</span></span>
<span data-ttu-id="0e73c-123">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0e73c-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="0e73c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e73c-124">CommonParameters</span></span>
<span data-ttu-id="0e73c-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e73c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e73c-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0e73c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e73c-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0e73c-127">INPUTS</span></span>

### <span data-ttu-id="0e73c-128">System.String</span><span class="sxs-lookup"><span data-stu-id="0e73c-128">System.String</span></span>

## <span data-ttu-id="0e73c-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0e73c-129">OUTPUTS</span></span>

### <span data-ttu-id="0e73c-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="0e73c-130">System.Void</span></span>

## <span data-ttu-id="0e73c-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0e73c-131">NOTES</span></span>

## <span data-ttu-id="0e73c-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0e73c-132">RELATED LINKS</span></span>
