---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccount.md
ms.openlocfilehash: 815b8a7feb22e754302c455c7666f8408c348c92
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052033"
---
# <span data-ttu-id="25d90-101">New-AzStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="25d90-101">New-AzStackEdgeStorageAccount</span></span>

## <span data-ttu-id="25d90-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="25d90-102">SYNOPSIS</span></span>
<span data-ttu-id="25d90-103">Tworzy nowe konto magazynu na brzegu na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="25d90-103">Creates a new Edge Storage account in the device.</span></span>

## <span data-ttu-id="25d90-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="25d90-104">SYNTAX</span></span>

```
New-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountCredentialName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-Cloud] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25d90-105">Opis</span><span class="sxs-lookup"><span data-stu-id="25d90-105">DESCRIPTION</span></span>
<span data-ttu-id="25d90-106">Polecenie cmdlet **New-AzStackEdgeStorageAccount** tworzy nowe konto magazynu na brzegu na urządzeniu ze stosem.</span><span class="sxs-lookup"><span data-stu-id="25d90-106">The **New-AzStackEdgeStorageAccount** cmdlet creates a new Edge Storage account in a Stack Edge device.</span></span> <span data-ttu-id="25d90-107">W przypadku urządzenia jedna krawędź konta magazynu może być mapowana tylko na jedno konto w chmurze.</span><span class="sxs-lookup"><span data-stu-id="25d90-107">For a device, one Edge Storage account can be mapped at most to only one Cloud Storage account.</span></span>

## <span data-ttu-id="25d90-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="25d90-108">EXAMPLES</span></span>

### <span data-ttu-id="25d90-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="25d90-109">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName dbEdge -Name edgestoragegacount1 -StorageAccountCredentialName cloudstorageaccount1 -Cloud
Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 0              OK     https://edgestoragegacount1.blob.dbEdge.microsoftdatabox.com/ cloudstorageaccount1     dbEdge     resourceGroupName
```

### <span data-ttu-id="25d90-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="25d90-110">Example 2</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName dbEdge -Name edgestoragegacount2 -StorageAccountCredentialName cloudstorageaccount2

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.dbEdge.microsoftdatabox.com/ cloudstorageaccount2     dbEdge     resourceGroupName
```

<span data-ttu-id="25d90-111">2 EdgeStorageAccounts na urządzeniu nie można udostępnić więcej niż 1 konta w chmurze</span><span class="sxs-lookup"><span data-stu-id="25d90-111">2 EdgeStorageAccounts on the device cannot share more than 1 Cloud Storage Account</span></span>

## <span data-ttu-id="25d90-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="25d90-112">PARAMETERS</span></span>

### <span data-ttu-id="25d90-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="25d90-113">-AsJob</span></span>
<span data-ttu-id="25d90-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="25d90-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="25d90-115">— Chmura</span><span class="sxs-lookup"><span data-stu-id="25d90-115">-Cloud</span></span>
<span data-ttu-id="25d90-116">W przypadku warstw będzie używana CloudStorageAccount</span><span class="sxs-lookup"><span data-stu-id="25d90-116">Will use a CloudStorageAccount for tiering</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25d90-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25d90-117">-DefaultProfile</span></span>
<span data-ttu-id="25d90-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="25d90-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25d90-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="25d90-119">-DeviceName</span></span>
<span data-ttu-id="25d90-120">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="25d90-120">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25d90-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="25d90-121">-Name</span></span>
<span data-ttu-id="25d90-122">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="25d90-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EdgeStorageAccount

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25d90-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25d90-123">-ResourceGroupName</span></span>
<span data-ttu-id="25d90-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="25d90-124">Resource Group Name</span></span>

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

### <span data-ttu-id="25d90-125">-StorageAccountCredentialName</span><span class="sxs-lookup"><span data-stu-id="25d90-125">-StorageAccountCredentialName</span></span>
<span data-ttu-id="25d90-126">Podaj nazwę zasobu istniejącej StorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="25d90-126">Provide existing StorageAccountCredential's Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25d90-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="25d90-127">-Confirm</span></span>
<span data-ttu-id="25d90-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25d90-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25d90-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25d90-129">-WhatIf</span></span>
<span data-ttu-id="25d90-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25d90-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="25d90-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="25d90-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25d90-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25d90-132">CommonParameters</span></span>
<span data-ttu-id="25d90-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25d90-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25d90-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="25d90-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25d90-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="25d90-135">INPUTS</span></span>

### <span data-ttu-id="25d90-136">System. String</span><span class="sxs-lookup"><span data-stu-id="25d90-136">System.String</span></span>

### <span data-ttu-id="25d90-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="25d90-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="25d90-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="25d90-138">OUTPUTS</span></span>

### <span data-ttu-id="25d90-139">Microsoft. Azure. PowerShell. polecenia. StackEdge. models. PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="25d90-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="25d90-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="25d90-140">NOTES</span></span>

## <span data-ttu-id="25d90-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="25d90-141">RELATED LINKS</span></span>
