---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: d4e9062b15e7d5ca7338e13cdcdf71506ba23e29
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052025"
---
# <span data-ttu-id="9b088-101">New-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="9b088-101">New-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="9b088-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9b088-102">SYNOPSIS</span></span>
<span data-ttu-id="9b088-103">Tworzy nowe poświadczenia dla konta magazynu programu Edge na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="9b088-103">Creates new credentials for an edge storage account on the device.</span></span>

## <span data-ttu-id="9b088-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9b088-104">SYNTAX</span></span>

```
New-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountType <String> -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b088-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9b088-105">DESCRIPTION</span></span>
<span data-ttu-id="9b088-106">Polecenie cmdlet **New-AzStackEdgeStorageAccountCredential** tworzy nowe poświadczenie konta magazynu Edge dla urządzenia brzegowego.</span><span class="sxs-lookup"><span data-stu-id="9b088-106">The **New-AzStackEdgeStorageAccountCredential** cmdlet creates a new edge storage account credential for a Stack Edge device.</span></span>

## <span data-ttu-id="9b088-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9b088-107">EXAMPLES</span></span>

### <span data-ttu-id="9b088-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9b088-108">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName device-name -Name storage-acount-credential-name -StorageAccountName storageAccountName -StorageAccountType BlobStorage -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                             StorageAccount    SslStatus  ResourceGroupName
--------------------------- ---------------------- ---------- ---------------------
storageAccountCredentalName storageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="9b088-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9b088-109">PARAMETERS</span></span>

### <span data-ttu-id="9b088-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9b088-110">-AsJob</span></span>
<span data-ttu-id="9b088-111">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="9b088-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9b088-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b088-112">-DefaultProfile</span></span>
<span data-ttu-id="9b088-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9b088-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b088-114">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="9b088-114">-DeviceName</span></span>
<span data-ttu-id="9b088-115">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="9b088-115">Device Name</span></span>

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

### <span data-ttu-id="9b088-116">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="9b088-116">-EncryptionKey</span></span>
<span data-ttu-id="9b088-117">Klucz szyfrowania urządzenia brzegowego</span><span class="sxs-lookup"><span data-stu-id="9b088-117">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="9b088-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9b088-118">-Name</span></span>
<span data-ttu-id="9b088-119">Nazwa konta magazynu, które ma być używane</span><span class="sxs-lookup"><span data-stu-id="9b088-119">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountCredentialName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b088-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b088-120">-ResourceGroupName</span></span>
<span data-ttu-id="9b088-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="9b088-121">Resource Group Name</span></span>

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

### <span data-ttu-id="9b088-122">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="9b088-122">-StorageAccountAccessKey</span></span>
<span data-ttu-id="9b088-123">Podaj klucz dostępu do konta magazynu</span><span class="sxs-lookup"><span data-stu-id="9b088-123">provide storage account access key</span></span>

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

### <span data-ttu-id="9b088-124">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="9b088-124">-StorageAccountType</span></span>
<span data-ttu-id="9b088-125">Możliwy typ dostępu do magazynu GeneralPurposeStorage, BlockStorage</span><span class="sxs-lookup"><span data-stu-id="9b088-125">Possible Storage Access type GeneralPurposeStorage, BlockStorage</span></span>

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

### <span data-ttu-id="9b088-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9b088-126">-Confirm</span></span>
<span data-ttu-id="9b088-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b088-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b088-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b088-128">-WhatIf</span></span>
<span data-ttu-id="9b088-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b088-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9b088-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9b088-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b088-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b088-131">CommonParameters</span></span>
<span data-ttu-id="9b088-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b088-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b088-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9b088-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b088-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9b088-134">INPUTS</span></span>

### <span data-ttu-id="9b088-135">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9b088-135">None</span></span>

## <span data-ttu-id="9b088-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9b088-136">OUTPUTS</span></span>

### <span data-ttu-id="9b088-137">Microsoft. Azure. PowerShell. polecenia. StackEdge. models. PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="9b088-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="9b088-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9b088-138">NOTES</span></span>

## <span data-ttu-id="9b088-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9b088-139">RELATED LINKS</span></span>
