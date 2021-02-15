---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappazurestoragepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppAzureStoragePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppAzureStoragePath.md
ms.openlocfilehash: 5571add1c12ac40279531274b47acfe67fc19734
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182451"
---
# <span data-ttu-id="a882c-101">New-AzWebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="a882c-101">New-AzWebAppAzureStoragePath</span></span>

## <span data-ttu-id="a882c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a882c-102">SYNOPSIS</span></span>
<span data-ttu-id="a882c-103">Tworzy obiekt reprezentujący ścieżkę magazynu platformy Azure, którą należy zmieścić w aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="a882c-103">Creates an object that represents an Azure Storage path to be mounted in a Web App.</span></span> <span data-ttu-id="a882c-104">Ma być używany jako parametr (-AzureStoragePath) do Set-AzWebApp i Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a882c-104">It is meant to be used as a parameter (-AzureStoragePath) to Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <span data-ttu-id="a882c-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a882c-105">SYNTAX</span></span>

```
New-AzWebAppAzureStoragePath -Name <String> -Type <AzureStorageType> -AccountName <String> -ShareName <String>
 -AccessKey <String> -MountPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a882c-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="a882c-106">DESCRIPTION</span></span>
<span data-ttu-id="a882c-107">Tworzy obiekt reprezentujący ścieżkę magazynu platformy Azure do montażu w aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="a882c-107">Creates an object that represent an Azure Storage path to be mounted inside a Web App.</span></span>

## <span data-ttu-id="a882c-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a882c-108">EXAMPLES</span></span>

### <span data-ttu-id="a882c-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a882c-109">Example 1</span></span>
```powershell
PS C:\> $storagePath1 = New-AzWebAppAzureStoragePath -Name "RemoteStorageAccount1" -AccountName "myaccount.files.core.windows.net" -Type AzureFiles -ShareName "someShareName" -AccessKey "some access key"
-MountPath "C:\myFolderInsideTheContainerWebApp" 

PS C:\> $storagePath2 = New-AzWebAppAzureStoragePath -Name "RemoteStorageAccount2" -AccountName "myaccount2.files.core.windows.net" -Type AzureFiles -ShareName "someShareName2" -AccessKey "some access key 2"
-MountPath "C:\myFolderInsideTheContainerWebApp2" 

PS C:\> Set-AzWebApp -ResourceGroup myresourcegroup -Name myapp -AzureStoragePath $storagepath1, $storagePath2
```

## <span data-ttu-id="a882c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a882c-110">PARAMETERS</span></span>

### <span data-ttu-id="a882c-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="a882c-111">-AccessKey</span></span>
<span data-ttu-id="a882c-112">Klucz dostępu do konta usługi Azure Storage</span><span class="sxs-lookup"><span data-stu-id="a882c-112">Access key to the Azure Storage account</span></span>

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

### <span data-ttu-id="a882c-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a882c-113">-AccountName</span></span>
<span data-ttu-id="a882c-114">Nazwa konta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a882c-114">Azure Storage account name.</span></span>
<span data-ttu-id="a882c-115">Na przykład: myfilestorageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="a882c-115">E.g.: myfilestorageaccount.file.core.windows.net</span></span>

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

### <span data-ttu-id="a882c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a882c-116">-DefaultProfile</span></span>
<span data-ttu-id="a882c-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a882c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a882c-118">— MountPath</span><span class="sxs-lookup"><span data-stu-id="a882c-118">-MountPath</span></span>
<span data-ttu-id="a882c-119">Ścieżka w kontenerze, w którym zostanie ujawniony udział określony przez usługę ShareName</span><span class="sxs-lookup"><span data-stu-id="a882c-119">Path in the container where the share specified by ShareName will be exposed</span></span>

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

### <span data-ttu-id="a882c-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a882c-120">-Name</span></span>
<span data-ttu-id="a882c-121">Identyfikator właściwości Magazyn platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a882c-121">The identifier of the Azure Storage property.</span></span>
<span data-ttu-id="a882c-122">Musi być unikatowy w aplikacji sieci Web lub w aplikacji Slot</span><span class="sxs-lookup"><span data-stu-id="a882c-122">Must be unique within the Web App or Slot</span></span>

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

### <span data-ttu-id="a882c-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="a882c-123">-ShareName</span></span>
<span data-ttu-id="a882c-124">Nazwa udziału do montażu na kontenerze</span><span class="sxs-lookup"><span data-stu-id="a882c-124">Name of the share to mount to the container</span></span>

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

### <span data-ttu-id="a882c-125">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="a882c-125">-Type</span></span>
<span data-ttu-id="a882c-126">Typ konta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a882c-126">Type of Azure Storage account.</span></span>
<span data-ttu-id="a882c-127">Kontenery systemu Windows obsługują tylko pliki platformy Azure</span><span class="sxs-lookup"><span data-stu-id="a882c-127">Windows Containers only supports Azure Files</span></span>

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

### <span data-ttu-id="a882c-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a882c-128">-Confirm</span></span>
<span data-ttu-id="a882c-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a882c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a882c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a882c-130">-WhatIf</span></span>
<span data-ttu-id="a882c-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a882c-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a882c-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a882c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a882c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a882c-133">CommonParameters</span></span>
<span data-ttu-id="a882c-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a882c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a882c-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a882c-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a882c-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a882c-136">INPUTS</span></span>

### <span data-ttu-id="a882c-137">Brak</span><span class="sxs-lookup"><span data-stu-id="a882c-137">None</span></span>

## <span data-ttu-id="a882c-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a882c-138">OUTPUTS</span></span>

### <span data-ttu-id="a882c-139">Microsoft.Azure.Commands.WebApps.Models.WebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="a882c-139">Microsoft.Azure.Commands.WebApps.Models.WebAppAzureStoragePath</span></span>

## <span data-ttu-id="a882c-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a882c-140">NOTES</span></span>

## <span data-ttu-id="a882c-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a882c-141">RELATED LINKS</span></span>
