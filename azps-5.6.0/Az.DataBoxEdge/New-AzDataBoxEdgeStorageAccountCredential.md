---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/new-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: 23fe08b273b95cd5ad3866437d131f432e6cee38
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978586"
---
# <span data-ttu-id="a7045-101">New-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="a7045-101">New-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="a7045-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7045-102">SYNOPSIS</span></span>
<span data-ttu-id="a7045-103">Tworzy nowe poświadczenia dla konta magazynu na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="a7045-103">Creates new credentials for an edge storage account on the device.</span></span>

## <span data-ttu-id="a7045-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a7045-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountType <String> -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7045-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a7045-105">DESCRIPTION</span></span>
<span data-ttu-id="a7045-106">Polecenie **cmdlet New-AzDataBoxEdgeStorageAccountCredential** tworzy nowe poświadczenia konta magazynu brzegowego dla urządzenia z krawędzią pola danych.</span><span class="sxs-lookup"><span data-stu-id="a7045-106">The **New-AzDataBoxEdgeStorageAccountCredential** cmdlet creates a new edge storage account credential for a Data Box Edge device.</span></span>

## <span data-ttu-id="a7045-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a7045-107">EXAMPLES</span></span>

### <span data-ttu-id="a7045-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a7045-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName device-name -Name storage-acount-credential-name -StorageAccountName storageAccountName -StorageAccountType BlobStorage -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                             StorageAccount    SslStatus  ResourceGroupName
--------------------------- ---------------------- ---------- ---------------------
storageAccountCredentalName storageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="a7045-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7045-109">PARAMETERS</span></span>

### <span data-ttu-id="a7045-110">— AsJob</span><span class="sxs-lookup"><span data-stu-id="a7045-110">-AsJob</span></span>
<span data-ttu-id="a7045-111">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a7045-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a7045-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7045-112">-DefaultProfile</span></span>
<span data-ttu-id="a7045-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a7045-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7045-114">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="a7045-114">-DeviceName</span></span>
<span data-ttu-id="a7045-115">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="a7045-115">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7045-116">— Klucz szyfrowania</span><span class="sxs-lookup"><span data-stu-id="a7045-116">-EncryptionKey</span></span>
<span data-ttu-id="a7045-117">Klucz szyfrowania urządzenia Edge</span><span class="sxs-lookup"><span data-stu-id="a7045-117">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7045-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a7045-118">-Name</span></span>
<span data-ttu-id="a7045-119">Nazwa konta miejsca do magazynowania, które ma zostać użyte</span><span class="sxs-lookup"><span data-stu-id="a7045-119">Name of the storage account to be used</span></span>

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

### <span data-ttu-id="a7045-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7045-120">-ResourceGroupName</span></span>
<span data-ttu-id="a7045-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a7045-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7045-122">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="a7045-122">-StorageAccountAccessKey</span></span>
<span data-ttu-id="a7045-123">Podaj klucz dostępu do konta magazynu</span><span class="sxs-lookup"><span data-stu-id="a7045-123">provide storage account access key</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7045-124">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="a7045-124">-StorageAccountType</span></span>
<span data-ttu-id="a7045-125">Możliwy typ dostępu do magazynu GeneralPurposeStorage, BlockStorage</span><span class="sxs-lookup"><span data-stu-id="a7045-125">Possible Storage Access type GeneralPurposeStorage, BlockStorage</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7045-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a7045-126">-Confirm</span></span>
<span data-ttu-id="a7045-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a7045-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7045-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7045-128">-WhatIf</span></span>
<span data-ttu-id="a7045-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7045-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a7045-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a7045-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7045-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7045-131">CommonParameters</span></span>
<span data-ttu-id="a7045-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7045-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7045-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a7045-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7045-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a7045-134">INPUTS</span></span>

### <span data-ttu-id="a7045-135">Brak</span><span class="sxs-lookup"><span data-stu-id="a7045-135">None</span></span>

## <span data-ttu-id="a7045-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a7045-136">OUTPUTS</span></span>

### <span data-ttu-id="a7045-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="a7045-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="a7045-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a7045-138">NOTES</span></span>

## <span data-ttu-id="a7045-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a7045-139">RELATED LINKS</span></span>
