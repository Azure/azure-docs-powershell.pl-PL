---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: f198db6a49e1f5165dcfcd4effd91106cc0df831
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222801"
---
# <span data-ttu-id="63fb3-101">Get-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="63fb3-101">Get-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="63fb3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="63fb3-102">SYNOPSIS</span></span>
<span data-ttu-id="63fb3-103">Pobiera poświadczenia konta magazynu odpowiadające kontu magazynu na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="63fb3-103">Gets the storage account credentials corresponding to the storage account on the device.</span></span>

## <span data-ttu-id="63fb3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="63fb3-104">SYNTAX</span></span>

### <span data-ttu-id="63fb3-105">ListParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="63fb3-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63fb3-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="63fb3-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="63fb3-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="63fb3-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63fb3-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="63fb3-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="63fb3-109">Opis</span><span class="sxs-lookup"><span data-stu-id="63fb3-109">DESCRIPTION</span></span>
<span data-ttu-id="63fb3-110">Polecenie cmdlet **Get-AzStackEdgeStorageAccountCredential** Pobiera poświadczenia konta magazynu dla odpowiedniego konta magazynu na urządzeniu z krawędziami stosu.</span><span class="sxs-lookup"><span data-stu-id="63fb3-110">The **Get-AzStackEdgeStorageAccountCredential** cmdlet gets the storage account credentials for the corresponding storage account on the Stack Edge device.</span></span> <span data-ttu-id="63fb3-111">Możesz określić nazwę, nazwę grupy zasobów i parametry nazwy urządzenia, aby uzyskać informacje o poświadczeniach określonego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="63fb3-111">You can specify Name, Resource Group Name and Device Name parameters to get information about a specific storage account credential.</span></span>

## <span data-ttu-id="63fb3-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="63fb3-112">EXAMPLES</span></span>

### <span data-ttu-id="63fb3-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="63fb3-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                          StorageAccount          SslStatus  ResourceGroupName
----------------------------- ---------------------- ---------- ---------------------
storageAccountCredentialName  StorageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="63fb3-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="63fb3-114">PARAMETERS</span></span>

### <span data-ttu-id="63fb3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63fb3-115">-DefaultProfile</span></span>
<span data-ttu-id="63fb3-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="63fb3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63fb3-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="63fb3-117">-DeviceName</span></span>
<span data-ttu-id="63fb3-118">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="63fb3-118">Device Name</span></span>

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

### <span data-ttu-id="63fb3-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="63fb3-119">-DeviceObject</span></span>
<span data-ttu-id="63fb3-120">Podaj odpowiedni obiekt urządzenia</span><span class="sxs-lookup"><span data-stu-id="63fb3-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="63fb3-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="63fb3-121">-Name</span></span>
<span data-ttu-id="63fb3-122">Nazwa konta magazynu, które ma być używane</span><span class="sxs-lookup"><span data-stu-id="63fb3-122">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: StorageAccountCredentialName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: StorageAccountCredentialName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63fb3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63fb3-123">-ResourceGroupName</span></span>
<span data-ttu-id="63fb3-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="63fb3-124">Resource Group Name</span></span>

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

### <span data-ttu-id="63fb3-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="63fb3-125">-ResourceId</span></span>
<span data-ttu-id="63fb3-126">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="63fb3-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="63fb3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63fb3-127">CommonParameters</span></span>
<span data-ttu-id="63fb3-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63fb3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63fb3-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="63fb3-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63fb3-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="63fb3-130">INPUTS</span></span>

### <span data-ttu-id="63fb3-131">Microsoft. Azure. PowerShell. polecenia. StackEdge. models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="63fb3-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="63fb3-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="63fb3-132">OUTPUTS</span></span>

### <span data-ttu-id="63fb3-133">Microsoft. Azure. PowerShell. polecenia. StackEdge. models. PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="63fb3-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="63fb3-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="63fb3-134">NOTES</span></span>

## <span data-ttu-id="63fb3-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="63fb3-135">RELATED LINKS</span></span>
