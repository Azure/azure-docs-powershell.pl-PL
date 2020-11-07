---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeShare.md
ms.openlocfilehash: 9bcc19d29bf372aaa0b1c59e23f53e80edde4d17
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893285"
---
# <span data-ttu-id="f6a62-101">Get-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="f6a62-101">Get-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="f6a62-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f6a62-102">SYNOPSIS</span></span>
<span data-ttu-id="f6a62-103">Pobiera dostępne akcje dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="f6a62-103">Gets the available shares for a device.</span></span>

## <span data-ttu-id="f6a62-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f6a62-104">SYNTAX</span></span>

### <span data-ttu-id="f6a62-105">ListParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f6a62-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6a62-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6a62-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6a62-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6a62-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6a62-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6a62-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeShare [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="f6a62-109">Opis</span><span class="sxs-lookup"><span data-stu-id="f6a62-109">DESCRIPTION</span></span>
<span data-ttu-id="f6a62-110">Polecenie cmdlet **Get-AzDataBoxEdgeShare** Pobiera dostępne akcje dla urządzenia z krawędziami pola danych.</span><span class="sxs-lookup"><span data-stu-id="f6a62-110">The **Get-AzDataBoxEdgeShare** cmdlet gets the available shares for a Data Box Edge device.</span></span> <span data-ttu-id="f6a62-111">Jeśli zostanie podana nazwa, otrzymasz nazwę Udostępnij.</span><span class="sxs-lookup"><span data-stu-id="f6a62-111">If Name is provided this will get the share by Name.</span></span>

## <span data-ttu-id="f6a62-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f6a62-112">EXAMPLES</span></span>

### <span data-ttu-id="f6a62-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f6a62-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-2    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-3    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-4    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="f6a62-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f6a62-114">PARAMETERS</span></span>

### <span data-ttu-id="f6a62-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6a62-115">-DefaultProfile</span></span>
<span data-ttu-id="f6a62-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f6a62-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6a62-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="f6a62-117">-DeviceName</span></span>
<span data-ttu-id="f6a62-118">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="f6a62-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6a62-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="f6a62-119">-DeviceObject</span></span>
<span data-ttu-id="f6a62-120">Podaj odpowiedni obiekt urządzenia</span><span class="sxs-lookup"><span data-stu-id="f6a62-120">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6a62-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f6a62-121">-Name</span></span>
<span data-ttu-id="f6a62-122">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="f6a62-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6a62-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6a62-123">-ResourceGroupName</span></span>
<span data-ttu-id="f6a62-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="f6a62-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6a62-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f6a62-125">-ResourceId</span></span>
<span data-ttu-id="f6a62-126">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="f6a62-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6a62-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6a62-127">CommonParameters</span></span>
<span data-ttu-id="f6a62-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6a62-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6a62-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6a62-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6a62-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f6a62-130">INPUTS</span></span>

### <span data-ttu-id="f6a62-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="f6a62-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="f6a62-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f6a62-132">OUTPUTS</span></span>

### <span data-ttu-id="f6a62-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="f6a62-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="f6a62-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f6a62-134">NOTES</span></span>

## <span data-ttu-id="f6a62-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f6a62-135">RELATED LINKS</span></span>
