---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccount.md
ms.openlocfilehash: 12f77d1c2b9590ef500e1df66d36929cd359a989
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893234"
---
# <span data-ttu-id="85722-101">New-AzDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="85722-101">New-AzDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="85722-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="85722-102">SYNOPSIS</span></span>
<span data-ttu-id="85722-103">Tworzy nowe konto magazynu na brzegu na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="85722-103">Creates a new Edge Storage account in the device.</span></span>

## <span data-ttu-id="85722-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="85722-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountCredentialName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-Cloud] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85722-105">Opis</span><span class="sxs-lookup"><span data-stu-id="85722-105">DESCRIPTION</span></span>
<span data-ttu-id="85722-106">Polecenie cmdlet **New-AzDataBoxEdgeStorageAccount** tworzy nowe konto magazynu Edge na urządzeniu z danymi na krawędziach pola danych.</span><span class="sxs-lookup"><span data-stu-id="85722-106">The **New-AzDataBoxEdgeStorageAccount** cmdlet creates a new Edge Storage account in a Data Box Edge device.</span></span> <span data-ttu-id="85722-107">W przypadku urządzenia jedna krawędź konta magazynu może być mapowana tylko na jedno konto w chmurze.</span><span class="sxs-lookup"><span data-stu-id="85722-107">For a device, one Edge Storage account can be mapped at most to only one Cloud Storage account.</span></span>

## <span data-ttu-id="85722-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="85722-108">EXAMPLES</span></span>

### <span data-ttu-id="85722-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="85722-109">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName dbEdge -Name edgestoragegacount1 -StorageAccountCredentialName cloudstorageaccount1 -Cloud
Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 0              OK     https://edgestoragegacount1.blob.dbEdge.microsoftdatabox.com/ cloudstorageaccount1     dbEdge     resourceGroupName
```

### <span data-ttu-id="85722-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="85722-110">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName dbEdge -Name edgestoragegacount2 -StorageAccountCredentialName cloudstorageaccount2

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.dbEdge.microsoftdatabox.com/ cloudstorageaccount2     dbEdge     resourceGroupName
```

<span data-ttu-id="85722-111">2 EdgeStorageAccounts na urządzeniu nie można udostępnić więcej niż 1 konta w chmurze</span><span class="sxs-lookup"><span data-stu-id="85722-111">2 EdgeStorageAccounts on the device cannot share more than 1 Cloud Storage Account</span></span>

## <span data-ttu-id="85722-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="85722-112">PARAMETERS</span></span>

### <span data-ttu-id="85722-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="85722-113">-AsJob</span></span>
<span data-ttu-id="85722-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="85722-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="85722-115">— Chmura</span><span class="sxs-lookup"><span data-stu-id="85722-115">-Cloud</span></span>
<span data-ttu-id="85722-116">W przypadku warstw będzie używana CloudStorageAccount</span><span class="sxs-lookup"><span data-stu-id="85722-116">Will use a CloudStorageAccount for tiering</span></span>

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

### <span data-ttu-id="85722-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85722-117">-DefaultProfile</span></span>
<span data-ttu-id="85722-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="85722-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85722-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="85722-119">-DeviceName</span></span>
<span data-ttu-id="85722-120">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="85722-120">Device Name</span></span>

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

### <span data-ttu-id="85722-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="85722-121">-Name</span></span>
<span data-ttu-id="85722-122">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="85722-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85722-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85722-123">-ResourceGroupName</span></span>
<span data-ttu-id="85722-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="85722-124">Resource Group Name</span></span>

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

### <span data-ttu-id="85722-125">-StorageAccountCredentialName</span><span class="sxs-lookup"><span data-stu-id="85722-125">-StorageAccountCredentialName</span></span>
<span data-ttu-id="85722-126">Podaj nazwę zasobu istniejącej StorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="85722-126">Provide existing StorageAccountCredential's Resource Name</span></span>

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

### <span data-ttu-id="85722-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="85722-127">-Confirm</span></span>
<span data-ttu-id="85722-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85722-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85722-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85722-129">-WhatIf</span></span>
<span data-ttu-id="85722-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85722-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="85722-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="85722-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85722-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85722-132">CommonParameters</span></span>
<span data-ttu-id="85722-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85722-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85722-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85722-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85722-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="85722-135">INPUTS</span></span>

### <span data-ttu-id="85722-136">System. String</span><span class="sxs-lookup"><span data-stu-id="85722-136">System.String</span></span>

### <span data-ttu-id="85722-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="85722-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="85722-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="85722-138">OUTPUTS</span></span>

### <span data-ttu-id="85722-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="85722-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="85722-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="85722-140">NOTES</span></span>

## <span data-ttu-id="85722-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="85722-141">RELATED LINKS</span></span>
