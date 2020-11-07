---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: E2A56E55-30A3-4A2F-80AE-9D166840909E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azremotedesktopfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzRemoteDesktopFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzRemoteDesktopFile.md
ms.openlocfilehash: 413977ee42b0edc2221cbbdcfd34b6130d40f74e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893801"
---
# <span data-ttu-id="fb7eb-101">Get-AzRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="fb7eb-101">Get-AzRemoteDesktopFile</span></span>

## <span data-ttu-id="fb7eb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fb7eb-102">SYNOPSIS</span></span>
<span data-ttu-id="fb7eb-103">Pobiera plik RDP.</span><span class="sxs-lookup"><span data-stu-id="fb7eb-103">Gets an .rdp file.</span></span>

## <span data-ttu-id="fb7eb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fb7eb-104">SYNTAX</span></span>

### <span data-ttu-id="fb7eb-105">Pobierz</span><span class="sxs-lookup"><span data-stu-id="fb7eb-105">Download</span></span>
```
Get-AzRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [-LocalPath] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb7eb-106">Wczesn</span><span class="sxs-lookup"><span data-stu-id="fb7eb-106">Launch</span></span>
```
Get-AzRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [[-LocalPath] <String>] [-Launch]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb7eb-107">Opis</span><span class="sxs-lookup"><span data-stu-id="fb7eb-107">DESCRIPTION</span></span>
<span data-ttu-id="fb7eb-108">Polecenie cmdlet **Get-AzRemoteDesktopFile** pobiera plik protokołu RDP (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="fb7eb-108">The **Get-AzRemoteDesktopFile** cmdlet gets a Remote Desktop Protocol (.rdp) file.</span></span>

## <span data-ttu-id="fb7eb-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fb7eb-109">EXAMPLES</span></span>

### <span data-ttu-id="fb7eb-110">Przykład 1: uzyskiwanie pliku pulpitu zdalnego</span><span class="sxs-lookup"><span data-stu-id="fb7eb-110">Example 1: Get a Remote Desktop file</span></span>
```
PS C:\> Get-AzRemoteDesktopFile -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -LocalPath "D:\RemoteDesktopFile07.rdp"
```

<span data-ttu-id="fb7eb-111">To polecenie pobiera plik pulpitu zdalnego dla maszyny wirtualnej o nazwie VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="fb7eb-111">This command gets the Remote Desktop file for the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="fb7eb-112">Polecenie zapisuje wynik w pliku o nazwie D:\RemoteDesktopFile07.rdp.</span><span class="sxs-lookup"><span data-stu-id="fb7eb-112">The command stores the result in the file named D:\RemoteDesktopFile07.rdp.</span></span>

## <span data-ttu-id="fb7eb-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fb7eb-113">PARAMETERS</span></span>

### <span data-ttu-id="fb7eb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb7eb-114">-DefaultProfile</span></span>
<span data-ttu-id="fb7eb-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fb7eb-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb7eb-116">-Uruchom</span><span class="sxs-lookup"><span data-stu-id="fb7eb-116">-Launch</span></span>
<span data-ttu-id="fb7eb-117">Wskazuje, że to polecenie cmdlet uruchamia pulpit zdalny po otrzymaniu pliku RDP.</span><span class="sxs-lookup"><span data-stu-id="fb7eb-117">Indicates that this cmdlet launches Remote Desktop after it gets the .rdp file.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Launch
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb7eb-118">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="fb7eb-118">-LocalPath</span></span>
<span data-ttu-id="fb7eb-119">Określa lokalną pełną ścieżkę, w której to polecenie cmdlet przechowuje plik RDP.</span><span class="sxs-lookup"><span data-stu-id="fb7eb-119">Specifies the local full path where this cmdlet stores the .rdp file.</span></span>

```yaml
Type: String
Parameter Sets: Download
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Launch
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb7eb-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fb7eb-120">-Name</span></span>
<span data-ttu-id="fb7eb-121">Określa nazwę zestawu dostępności, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb7eb-121">Specifies the name of the availability set that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb7eb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb7eb-122">-ResourceGroupName</span></span>
<span data-ttu-id="fb7eb-123">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fb7eb-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="fb7eb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb7eb-124">CommonParameters</span></span>
<span data-ttu-id="fb7eb-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb7eb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb7eb-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb7eb-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb7eb-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fb7eb-127">INPUTS</span></span>

### <span data-ttu-id="fb7eb-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="fb7eb-128">None</span></span>
<span data-ttu-id="fb7eb-129">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="fb7eb-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fb7eb-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fb7eb-130">OUTPUTS</span></span>

## <span data-ttu-id="fb7eb-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fb7eb-131">NOTES</span></span>

## <span data-ttu-id="fb7eb-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fb7eb-132">RELATED LINKS</span></span>

