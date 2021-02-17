---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: 54d74b40230f67a31e023ef4933d3480bc5c2b42
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196618"
---
# <span data-ttu-id="03848-101">New-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="03848-101">New-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="03848-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03848-102">SYNOPSIS</span></span>
<span data-ttu-id="03848-103">Tworzy nowe poświadczenia dla konta magazynu na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="03848-103">Creates new credentials for an edge storage account on the device.</span></span>

## <span data-ttu-id="03848-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="03848-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountType <String> -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03848-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="03848-105">DESCRIPTION</span></span>
<span data-ttu-id="03848-106">Polecenie **cmdlet New-AzDataBoxEdgeStorageAccountCredential** tworzy nowe poświadczenia konta magazynu brzegowego dla urządzenia z krawędzią pola danych.</span><span class="sxs-lookup"><span data-stu-id="03848-106">The **New-AzDataBoxEdgeStorageAccountCredential** cmdlet creates a new edge storage account credential for a Data Box Edge device.</span></span>

## <span data-ttu-id="03848-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="03848-107">EXAMPLES</span></span>

### <span data-ttu-id="03848-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="03848-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName device-name -Name storage-acount-credential-name -StorageAccountName storageAccountName -StorageAccountType BlobStorage -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                             StorageAccount    SslStatus  ResourceGroupName
--------------------------- ---------------------- ---------- ---------------------
storageAccountCredentalName storageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="03848-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03848-109">PARAMETERS</span></span>

### <span data-ttu-id="03848-110">— AsJob</span><span class="sxs-lookup"><span data-stu-id="03848-110">-AsJob</span></span>
<span data-ttu-id="03848-111">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="03848-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="03848-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03848-112">-DefaultProfile</span></span>
<span data-ttu-id="03848-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="03848-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03848-114">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="03848-114">-DeviceName</span></span>
<span data-ttu-id="03848-115">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="03848-115">Device Name</span></span>

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

### <span data-ttu-id="03848-116">— Klucz szyfrowania</span><span class="sxs-lookup"><span data-stu-id="03848-116">-EncryptionKey</span></span>
<span data-ttu-id="03848-117">Klucz szyfrowania urządzenia Edge</span><span class="sxs-lookup"><span data-stu-id="03848-117">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="03848-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="03848-118">-Name</span></span>
<span data-ttu-id="03848-119">Nazwa konta miejsca do magazynowania, które ma zostać użyte</span><span class="sxs-lookup"><span data-stu-id="03848-119">Name of the storage account to be used</span></span>

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

### <span data-ttu-id="03848-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03848-120">-ResourceGroupName</span></span>
<span data-ttu-id="03848-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="03848-121">Resource Group Name</span></span>

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

### <span data-ttu-id="03848-122">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="03848-122">-StorageAccountAccessKey</span></span>
<span data-ttu-id="03848-123">Podaj klucz dostępu do konta magazynu</span><span class="sxs-lookup"><span data-stu-id="03848-123">provide storage account access key</span></span>

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

### <span data-ttu-id="03848-124">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="03848-124">-StorageAccountType</span></span>
<span data-ttu-id="03848-125">Możliwy typ dostępu do magazynu GeneralPurposeStorage, BlockStorage</span><span class="sxs-lookup"><span data-stu-id="03848-125">Possible Storage Access type GeneralPurposeStorage, BlockStorage</span></span>

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

### <span data-ttu-id="03848-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="03848-126">-Confirm</span></span>
<span data-ttu-id="03848-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="03848-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03848-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03848-128">-WhatIf</span></span>
<span data-ttu-id="03848-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03848-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="03848-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="03848-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03848-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03848-131">CommonParameters</span></span>
<span data-ttu-id="03848-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03848-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03848-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="03848-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03848-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03848-134">INPUTS</span></span>

### <span data-ttu-id="03848-135">Brak</span><span class="sxs-lookup"><span data-stu-id="03848-135">None</span></span>

## <span data-ttu-id="03848-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="03848-136">OUTPUTS</span></span>

### <span data-ttu-id="03848-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="03848-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="03848-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="03848-138">NOTES</span></span>

## <span data-ttu-id="03848-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="03848-139">RELATED LINKS</span></span>
