---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: 399c4030f9cd3efd04ec41ce3ab3475f0a660f4f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893230"
---
# <span data-ttu-id="87d53-101">New-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="87d53-101">New-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="87d53-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="87d53-102">SYNOPSIS</span></span>
<span data-ttu-id="87d53-103">Tworzy nowe poświadczenia dla konta magazynu programu Edge na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="87d53-103">Creates new credentials for an edge storage account on the device.</span></span>

## <span data-ttu-id="87d53-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="87d53-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountType <String> -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87d53-105">Opis</span><span class="sxs-lookup"><span data-stu-id="87d53-105">DESCRIPTION</span></span>
<span data-ttu-id="87d53-106">Polecenie cmdlet **New-AzDataBoxEdgeStorageAccountCredential** tworzy nowe poświadczenie konta magazynu Edge dla urządzenia z krawędzią pola danych.</span><span class="sxs-lookup"><span data-stu-id="87d53-106">The **New-AzDataBoxEdgeStorageAccountCredential** cmdlet creates a new edge storage account credential for a Data Box Edge device.</span></span>

## <span data-ttu-id="87d53-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="87d53-107">EXAMPLES</span></span>

### <span data-ttu-id="87d53-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="87d53-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName device-name -Name storage-acount-credential-name -StorageAccountName storageAccountName -StorageAccountType BlobStorage -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                             StorageAccount    SslStatus  ResourceGroupName
--------------------------- ---------------------- ---------- ---------------------
storageAccountCredentalName storageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="87d53-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="87d53-109">PARAMETERS</span></span>

### <span data-ttu-id="87d53-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="87d53-110">-AsJob</span></span>
<span data-ttu-id="87d53-111">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="87d53-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="87d53-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87d53-112">-DefaultProfile</span></span>
<span data-ttu-id="87d53-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="87d53-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87d53-114">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="87d53-114">-DeviceName</span></span>
<span data-ttu-id="87d53-115">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="87d53-115">Device Name</span></span>

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

### <span data-ttu-id="87d53-116">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="87d53-116">-EncryptionKey</span></span>
<span data-ttu-id="87d53-117">Klucz szyfrowania urządzenia brzegowego</span><span class="sxs-lookup"><span data-stu-id="87d53-117">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="87d53-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="87d53-118">-Name</span></span>
<span data-ttu-id="87d53-119">Nazwa konta magazynu, które ma być używane</span><span class="sxs-lookup"><span data-stu-id="87d53-119">Name of the storage account to be used</span></span>

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

### <span data-ttu-id="87d53-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87d53-120">-ResourceGroupName</span></span>
<span data-ttu-id="87d53-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="87d53-121">Resource Group Name</span></span>

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

### <span data-ttu-id="87d53-122">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="87d53-122">-StorageAccountAccessKey</span></span>
<span data-ttu-id="87d53-123">Podaj klucz dostępu do konta magazynu</span><span class="sxs-lookup"><span data-stu-id="87d53-123">provide storage account access key</span></span>

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

### <span data-ttu-id="87d53-124">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="87d53-124">-StorageAccountType</span></span>
<span data-ttu-id="87d53-125">Możliwy typ dostępu do magazynu GeneralPurposeStorage, BlockStorage</span><span class="sxs-lookup"><span data-stu-id="87d53-125">Possible Storage Access type GeneralPurposeStorage, BlockStorage</span></span>

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

### <span data-ttu-id="87d53-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="87d53-126">-Confirm</span></span>
<span data-ttu-id="87d53-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87d53-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87d53-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87d53-128">-WhatIf</span></span>
<span data-ttu-id="87d53-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87d53-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="87d53-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="87d53-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87d53-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87d53-131">CommonParameters</span></span>
<span data-ttu-id="87d53-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87d53-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87d53-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="87d53-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87d53-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="87d53-134">INPUTS</span></span>

### <span data-ttu-id="87d53-135">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="87d53-135">None</span></span>

## <span data-ttu-id="87d53-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="87d53-136">OUTPUTS</span></span>

### <span data-ttu-id="87d53-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="87d53-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="87d53-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="87d53-138">NOTES</span></span>

## <span data-ttu-id="87d53-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="87d53-139">RELATED LINKS</span></span>
