---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappazurestoragepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppAzureStoragePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppAzureStoragePath.md
ms.openlocfilehash: 5571add1c12ac40279531274b47acfe67fc19734
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93896513"
---
# <span data-ttu-id="12cd4-101">New-AzWebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="12cd4-101">New-AzWebAppAzureStoragePath</span></span>

## <span data-ttu-id="12cd4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="12cd4-102">SYNOPSIS</span></span>
<span data-ttu-id="12cd4-103">Tworzy obiekt reprezentujący ścieżkę usługi Azure Storage, która będzie instalowana w aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="12cd4-103">Creates an object that represents an Azure Storage path to be mounted in a Web App.</span></span> <span data-ttu-id="12cd4-104">Jest ona przeznaczona do Set-AzWebApp i Set-AzWebAppSlot za pomocą parametru (-AzureStoragePath).</span><span class="sxs-lookup"><span data-stu-id="12cd4-104">It is meant to be used as a parameter (-AzureStoragePath) to Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <span data-ttu-id="12cd4-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="12cd4-105">SYNTAX</span></span>

```
New-AzWebAppAzureStoragePath -Name <String> -Type <AzureStorageType> -AccountName <String> -ShareName <String>
 -AccessKey <String> -MountPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="12cd4-106">Opis</span><span class="sxs-lookup"><span data-stu-id="12cd4-106">DESCRIPTION</span></span>
<span data-ttu-id="12cd4-107">Tworzy obiekt reprezentujący ścieżkę usługi Azure Storage, która będzie instalowana w aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="12cd4-107">Creates an object that represent an Azure Storage path to be mounted inside a Web App.</span></span>

## <span data-ttu-id="12cd4-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="12cd4-108">EXAMPLES</span></span>

### <span data-ttu-id="12cd4-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="12cd4-109">Example 1</span></span>
```powershell
PS C:\> $storagePath1 = New-AzWebAppAzureStoragePath -Name "RemoteStorageAccount1" -AccountName "myaccount.files.core.windows.net" -Type AzureFiles -ShareName "someShareName" -AccessKey "some access key"
-MountPath "C:\myFolderInsideTheContainerWebApp" 

PS C:\> $storagePath2 = New-AzWebAppAzureStoragePath -Name "RemoteStorageAccount2" -AccountName "myaccount2.files.core.windows.net" -Type AzureFiles -ShareName "someShareName2" -AccessKey "some access key 2"
-MountPath "C:\myFolderInsideTheContainerWebApp2" 

PS C:\> Set-AzWebApp -ResourceGroup myresourcegroup -Name myapp -AzureStoragePath $storagepath1, $storagePath2
```

## <span data-ttu-id="12cd4-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="12cd4-110">PARAMETERS</span></span>

### <span data-ttu-id="12cd4-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="12cd4-111">-AccessKey</span></span>
<span data-ttu-id="12cd4-112">Klucz dostępu do konta usługi Azure Storage</span><span class="sxs-lookup"><span data-stu-id="12cd4-112">Access key to the Azure Storage account</span></span>

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

### <span data-ttu-id="12cd4-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="12cd4-113">-AccountName</span></span>
<span data-ttu-id="12cd4-114">Nazwa konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="12cd4-114">Azure Storage account name.</span></span>
<span data-ttu-id="12cd4-115">Na przykład: myfilestorageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="12cd4-115">E.g.: myfilestorageaccount.file.core.windows.net</span></span>

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

### <span data-ttu-id="12cd4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12cd4-116">-DefaultProfile</span></span>
<span data-ttu-id="12cd4-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="12cd4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12cd4-118">-MountPath</span><span class="sxs-lookup"><span data-stu-id="12cd4-118">-MountPath</span></span>
<span data-ttu-id="12cd4-119">Ścieżka w kontenerze, w którym zostanie uwidoczniony udział określony przez nazwa_udziału.</span><span class="sxs-lookup"><span data-stu-id="12cd4-119">Path in the container where the share specified by ShareName will be exposed</span></span>

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

### <span data-ttu-id="12cd4-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="12cd4-120">-Name</span></span>
<span data-ttu-id="12cd4-121">Identyfikator właściwości magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="12cd4-121">The identifier of the Azure Storage property.</span></span>
<span data-ttu-id="12cd4-122">Musi być unikatowa w aplikacji sieci Web lub gnieździe</span><span class="sxs-lookup"><span data-stu-id="12cd4-122">Must be unique within the Web App or Slot</span></span>

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

### <span data-ttu-id="12cd4-123">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="12cd4-123">-ShareName</span></span>
<span data-ttu-id="12cd4-124">Nazwa udziału do zainstalowania w kontenerze</span><span class="sxs-lookup"><span data-stu-id="12cd4-124">Name of the share to mount to the container</span></span>

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

### <span data-ttu-id="12cd4-125">-Type</span><span class="sxs-lookup"><span data-stu-id="12cd4-125">-Type</span></span>
<span data-ttu-id="12cd4-126">Typ konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="12cd4-126">Type of Azure Storage account.</span></span>
<span data-ttu-id="12cd4-127">Kontenery systemu Windows obsługują tylko pliki platformy Azure</span><span class="sxs-lookup"><span data-stu-id="12cd4-127">Windows Containers only supports Azure Files</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.AzureStorageType
Parameter Sets: (All)
Aliases:
Accepted values: AzureFiles, AzureBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12cd4-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="12cd4-128">-Confirm</span></span>
<span data-ttu-id="12cd4-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12cd4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12cd4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12cd4-130">-WhatIf</span></span>
<span data-ttu-id="12cd4-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12cd4-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="12cd4-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="12cd4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12cd4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12cd4-133">CommonParameters</span></span>
<span data-ttu-id="12cd4-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12cd4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12cd4-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12cd4-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12cd4-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="12cd4-136">INPUTS</span></span>

### <span data-ttu-id="12cd4-137">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="12cd4-137">None</span></span>

## <span data-ttu-id="12cd4-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="12cd4-138">OUTPUTS</span></span>

### <span data-ttu-id="12cd4-139">Microsoft. Azure. Commands. webapps. modele. WebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="12cd4-139">Microsoft.Azure.Commands.WebApps.Models.WebAppAzureStoragePath</span></span>

## <span data-ttu-id="12cd4-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="12cd4-140">NOTES</span></span>

## <span data-ttu-id="12cd4-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="12cd4-141">RELATED LINKS</span></span>
