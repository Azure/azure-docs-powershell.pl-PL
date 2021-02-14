---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 022BBF5F-AFF1-45D5-9153-872779FFBAF4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/restore-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Restore-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Restore-AzApiManagement.md
ms.openlocfilehash: d99db4c9fe2c69e2177d9b35e15b49957e910014
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197154"
---
# <span data-ttu-id="55571-101">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="55571-101">Restore-AzApiManagement</span></span>

## <span data-ttu-id="55571-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55571-102">SYNOPSIS</span></span>
<span data-ttu-id="55571-103">Przywraca usługę zarządzania interfejsem API z określonego obiektu blob magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="55571-103">Restores an API Management Service from the specified Azure storage blob.</span></span>

## <span data-ttu-id="55571-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="55571-104">SYNTAX</span></span>

```
Restore-AzApiManagement -ResourceGroupName <String> -Name <String> [-StorageContext] <IStorageContext>
 -SourceContainerName <String> -SourceBlobName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="55571-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="55571-105">DESCRIPTION</span></span>
<span data-ttu-id="55571-106">Polecenie cmdlet **Restore-AzApiManagement** przywraca usługę zarządzania interfejsem API z określonej kopii zapasowej, która jest magazynowana w obiekcie blob azurestorage.</span><span class="sxs-lookup"><span data-stu-id="55571-106">The **Restore-AzApiManagement** cmdlet restores an API Management Service from the specified backup residing in an Azurestorage blob.</span></span>

## <span data-ttu-id="55571-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="55571-107">EXAMPLES</span></span>

### <span data-ttu-id="55571-108">Przykład 1. Przywracanie usługi zarządzania interfejsem API</span><span class="sxs-lookup"><span data-stu-id="55571-108">Example 1: Restore an API Management service</span></span>
```
PS C:\>New-AzStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Restore-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "RestoredContosoApi" -StorageContext $StorageContext -SourceContainerName "ContosoBackups" -SourceBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="55571-109">To polecenie przywraca usługę zarządzania interfejsami API z obiektu blob magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="55571-109">This command restores an API Management service from Azure storage blob.</span></span>

## <span data-ttu-id="55571-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="55571-110">PARAMETERS</span></span>

### <span data-ttu-id="55571-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55571-111">-DefaultProfile</span></span>
<span data-ttu-id="55571-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="55571-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55571-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="55571-113">-Name</span></span>
<span data-ttu-id="55571-114">Określa nazwę wystąpienia zarządzania interfejsem API, które zostanie przywrócone przy użyciu kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="55571-114">Specifies the name of the API Management instance that will be restored with the backup.</span></span>

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

### <span data-ttu-id="55571-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="55571-115">-PassThru</span></span>
<span data-ttu-id="55571-116">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="55571-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="55571-117">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="55571-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="55571-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55571-118">-ResourceGroupName</span></span>
<span data-ttu-id="55571-119">Określa nazwę grupy zasobów, w której istnieje zarządzanie interfejsami API.</span><span class="sxs-lookup"><span data-stu-id="55571-119">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="55571-120">-SourceBlobName</span><span class="sxs-lookup"><span data-stu-id="55571-120">-SourceBlobName</span></span>
<span data-ttu-id="55571-121">Określa nazwę obiektu blob źródłowego kopii zapasowej magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="55571-121">Specifies the name of the Azure storage backup source blob.</span></span>

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

### <span data-ttu-id="55571-122">-SourceContainerName</span><span class="sxs-lookup"><span data-stu-id="55571-122">-SourceContainerName</span></span>
<span data-ttu-id="55571-123">Określa nazwę kontenera źródłowego kopii zapasowej magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="55571-123">Specifies the name of the Azure storage backup source container.</span></span>

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

### <span data-ttu-id="55571-124">- StorageContext</span><span class="sxs-lookup"><span data-stu-id="55571-124">-StorageContext</span></span>
<span data-ttu-id="55571-125">Określa kontekst połączenia magazynu.</span><span class="sxs-lookup"><span data-stu-id="55571-125">Specifies the storage connection context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55571-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55571-126">CommonParameters</span></span>
<span data-ttu-id="55571-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55571-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55571-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="55571-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55571-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="55571-129">INPUTS</span></span>

### <span data-ttu-id="55571-130">System.String</span><span class="sxs-lookup"><span data-stu-id="55571-130">System.String</span></span>

## <span data-ttu-id="55571-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="55571-131">OUTPUTS</span></span>

### <span data-ttu-id="55571-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="55571-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="55571-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="55571-133">NOTES</span></span>

## <span data-ttu-id="55571-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="55571-134">RELATED LINKS</span></span>

[<span data-ttu-id="55571-135">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="55571-135">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="55571-136">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="55571-136">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="55571-137">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="55571-137">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="55571-138">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="55571-138">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)


