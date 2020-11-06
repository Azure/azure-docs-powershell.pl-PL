---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E2A56E55-30A3-4A2F-80AE-9D166840909E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermremotedesktopfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmRemoteDesktopFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmRemoteDesktopFile.md
ms.openlocfilehash: e6f3ba75247d8b5358e2a97c8bc635bbf805baec
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541868"
---
# <span data-ttu-id="d160b-101">Get-AzureRmRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="d160b-101">Get-AzureRmRemoteDesktopFile</span></span>

## <span data-ttu-id="d160b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d160b-102">SYNOPSIS</span></span>
<span data-ttu-id="d160b-103">Pobiera plik RDP.</span><span class="sxs-lookup"><span data-stu-id="d160b-103">Gets an .rdp file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d160b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d160b-104">SYNTAX</span></span>

### <span data-ttu-id="d160b-105">Pobierz</span><span class="sxs-lookup"><span data-stu-id="d160b-105">Download</span></span>
```
Get-AzureRmRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [-LocalPath] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d160b-106">Wczesn</span><span class="sxs-lookup"><span data-stu-id="d160b-106">Launch</span></span>
```
Get-AzureRmRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [[-LocalPath] <String>] [-Launch]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d160b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d160b-107">DESCRIPTION</span></span>
<span data-ttu-id="d160b-108">Polecenie cmdlet **Get-AzureRmRemoteDesktopFile** pobiera plik protokołu RDP (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="d160b-108">The **Get-AzureRmRemoteDesktopFile** cmdlet gets a Remote Desktop Protocol (.rdp) file.</span></span>

## <span data-ttu-id="d160b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d160b-109">EXAMPLES</span></span>

### <span data-ttu-id="d160b-110">Przykład 1: uzyskiwanie pliku pulpitu zdalnego</span><span class="sxs-lookup"><span data-stu-id="d160b-110">Example 1: Get a Remote Desktop file</span></span>
```
PS C:\> Get-AzureRmRemoteDesktopFile -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -LocalPath "D:\RemoteDesktopFile07.rdp"
```

<span data-ttu-id="d160b-111">To polecenie pobiera plik pulpitu zdalnego dla maszyny wirtualnej o nazwie VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="d160b-111">This command gets the Remote Desktop file for the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="d160b-112">Polecenie zapisuje wynik w pliku o nazwie D:\RemoteDesktopFile07.rdp.</span><span class="sxs-lookup"><span data-stu-id="d160b-112">The command stores the result in the file named D:\RemoteDesktopFile07.rdp.</span></span>

## <span data-ttu-id="d160b-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d160b-113">PARAMETERS</span></span>

### <span data-ttu-id="d160b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d160b-114">-DefaultProfile</span></span>
<span data-ttu-id="d160b-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d160b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d160b-116">-Uruchom</span><span class="sxs-lookup"><span data-stu-id="d160b-116">-Launch</span></span>
<span data-ttu-id="d160b-117">Wskazuje, że to polecenie cmdlet uruchamia pulpit zdalny po otrzymaniu pliku RDP.</span><span class="sxs-lookup"><span data-stu-id="d160b-117">Indicates that this cmdlet launches Remote Desktop after it gets the .rdp file.</span></span>

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

### <span data-ttu-id="d160b-118">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="d160b-118">-LocalPath</span></span>
<span data-ttu-id="d160b-119">Określa lokalną pełną ścieżkę, w której to polecenie cmdlet przechowuje plik RDP.</span><span class="sxs-lookup"><span data-stu-id="d160b-119">Specifies the local full path where this cmdlet stores the .rdp file.</span></span>

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

### <span data-ttu-id="d160b-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d160b-120">-Name</span></span>
<span data-ttu-id="d160b-121">Określa nazwę zestawu dostępności, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d160b-121">Specifies the name of the availability set that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d160b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d160b-122">-ResourceGroupName</span></span>
<span data-ttu-id="d160b-123">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d160b-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d160b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d160b-124">CommonParameters</span></span>
<span data-ttu-id="d160b-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d160b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d160b-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d160b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d160b-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d160b-127">INPUTS</span></span>

### <span data-ttu-id="d160b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d160b-128">System.String</span></span>

## <span data-ttu-id="d160b-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d160b-129">OUTPUTS</span></span>

### <span data-ttu-id="d160b-130">System. void</span><span class="sxs-lookup"><span data-stu-id="d160b-130">System.Void</span></span>

## <span data-ttu-id="d160b-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d160b-131">NOTES</span></span>

## <span data-ttu-id="d160b-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d160b-132">RELATED LINKS</span></span>
