---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeShare.md
ms.openlocfilehash: 0e0d0e3b2dfca824d66a9a75f3e22438335c97db
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222803"
---
# <span data-ttu-id="c99ff-101">Get-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="c99ff-101">Get-AzStackEdgeShare</span></span>

## <span data-ttu-id="c99ff-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c99ff-102">SYNOPSIS</span></span>
<span data-ttu-id="c99ff-103">Pobiera dostępne akcje dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="c99ff-103">Gets the available shares for a device.</span></span>

## <span data-ttu-id="c99ff-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c99ff-104">SYNTAX</span></span>

### <span data-ttu-id="c99ff-105">ListParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c99ff-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c99ff-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c99ff-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c99ff-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c99ff-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c99ff-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c99ff-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeShare [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="c99ff-109">Opis</span><span class="sxs-lookup"><span data-stu-id="c99ff-109">DESCRIPTION</span></span>
<span data-ttu-id="c99ff-110">Polecenie cmdlet **Get-AzStackEdgeShare** Pobiera dostępne akcje dla urządzenia ze stosem.</span><span class="sxs-lookup"><span data-stu-id="c99ff-110">The **Get-AzStackEdgeShare** cmdlet gets the available shares for a Stack Edge device.</span></span> <span data-ttu-id="c99ff-111">Jeśli zostanie podana nazwa, otrzymasz nazwę Udostępnij.</span><span class="sxs-lookup"><span data-stu-id="c99ff-111">If Name is provided this will get the share by Name.</span></span>

## <span data-ttu-id="c99ff-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c99ff-112">EXAMPLES</span></span>

### <span data-ttu-id="c99ff-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c99ff-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-2    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-3    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-4    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="c99ff-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c99ff-114">PARAMETERS</span></span>

### <span data-ttu-id="c99ff-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c99ff-115">-DefaultProfile</span></span>
<span data-ttu-id="c99ff-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c99ff-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c99ff-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="c99ff-117">-DeviceName</span></span>
<span data-ttu-id="c99ff-118">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="c99ff-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c99ff-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="c99ff-119">-DeviceObject</span></span>
<span data-ttu-id="c99ff-120">Podaj odpowiedni obiekt urządzenia</span><span class="sxs-lookup"><span data-stu-id="c99ff-120">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c99ff-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c99ff-121">-Name</span></span>
<span data-ttu-id="c99ff-122">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="c99ff-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: EdgeShareName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c99ff-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c99ff-123">-ResourceGroupName</span></span>
<span data-ttu-id="c99ff-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="c99ff-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c99ff-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c99ff-125">-ResourceId</span></span>
<span data-ttu-id="c99ff-126">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="c99ff-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c99ff-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c99ff-127">CommonParameters</span></span>
<span data-ttu-id="c99ff-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c99ff-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c99ff-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c99ff-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c99ff-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c99ff-130">INPUTS</span></span>

### <span data-ttu-id="c99ff-131">Microsoft. Azure. PowerShell. polecenia. StackEdge. models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="c99ff-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="c99ff-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c99ff-132">OUTPUTS</span></span>

### <span data-ttu-id="c99ff-133">Microsoft. Azure. PowerShell. polecenia. StackEdge. models. PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="c99ff-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="c99ff-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c99ff-134">NOTES</span></span>

## <span data-ttu-id="c99ff-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c99ff-135">RELATED LINKS</span></span>
