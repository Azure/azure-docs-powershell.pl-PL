---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 022BBF5F-AFF1-45D5-9153-872779FFBAF4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/restore-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Restore-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Restore-AzureRmApiManagement.md
ms.openlocfilehash: 1fc22563949f44882d0b6ed1f864d217faacff9d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550391"
---
# <span data-ttu-id="7ea9f-101">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="7ea9f-101">Restore-AzureRmApiManagement</span></span>

## <span data-ttu-id="7ea9f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7ea9f-102">SYNOPSIS</span></span>
<span data-ttu-id="7ea9f-103">Przywraca usługę zarządzania interfejsem API z określonego obiektu blob magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7ea9f-103">Restores an API Management Service from the specified Azure storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ea9f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7ea9f-104">SYNTAX</span></span>

```
Restore-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-StorageContext] <IStorageContext>
 -SourceContainerName <String> -SourceBlobName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7ea9f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7ea9f-105">DESCRIPTION</span></span>
<span data-ttu-id="7ea9f-106">Polecenie cmdlet **Restore-AzureRmApiManagement** przywraca usługę zarządzania interfejsem API z określonej kopii zapasowej znajdującej się w obiekcie blob Azurestorage.</span><span class="sxs-lookup"><span data-stu-id="7ea9f-106">The **Restore-AzureRmApiManagement** cmdlet restores an API Management Service from the specified backup residing in an Azurestorage blob.</span></span>

## <span data-ttu-id="7ea9f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7ea9f-107">EXAMPLES</span></span>

### <span data-ttu-id="7ea9f-108">Przykład 1: Przywracanie usługi zarządzania interfejsem API</span><span class="sxs-lookup"><span data-stu-id="7ea9f-108">Example 1: Restore an API Management service</span></span>
```
PS C:\>New-AzureRmStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzureRmStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzureStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Restore-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "RestoredContosoApi" -StorageContext $StorageContext -SourceContainerName "ContosoBackups" -SourceBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="7ea9f-109">To polecenie przywraca usługę zarządzania interfejsem API z obiektu blob magazynu Azure.</span><span class="sxs-lookup"><span data-stu-id="7ea9f-109">This command restores an API Management service from Azure storage blob.</span></span>

## <span data-ttu-id="7ea9f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7ea9f-110">PARAMETERS</span></span>

### <span data-ttu-id="7ea9f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ea9f-111">-DefaultProfile</span></span>
<span data-ttu-id="7ea9f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7ea9f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea9f-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7ea9f-113">-Name</span></span>
<span data-ttu-id="7ea9f-114">Określa nazwę wystąpienia zarządzania interfejsem API, które zostanie przywrócone przy użyciu kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="7ea9f-114">Specifies the name of the API Management instance that will be restored with the backup.</span></span>

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

### <span data-ttu-id="7ea9f-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7ea9f-115">-PassThru</span></span>
<span data-ttu-id="7ea9f-116">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="7ea9f-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7ea9f-117">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="7ea9f-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7ea9f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ea9f-118">-ResourceGroupName</span></span>
<span data-ttu-id="7ea9f-119">Określa nazwę grupy zasobów, pod którą istnieje zarządzanie interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="7ea9f-119">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="7ea9f-120">-SourceBlobName</span><span class="sxs-lookup"><span data-stu-id="7ea9f-120">-SourceBlobName</span></span>
<span data-ttu-id="7ea9f-121">Określa nazwę obiektu BLOB źródła kopii zapasowej Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="7ea9f-121">Specifies the name of the Azure storage backup source blob.</span></span>

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

### <span data-ttu-id="7ea9f-122">-SourceContainerName</span><span class="sxs-lookup"><span data-stu-id="7ea9f-122">-SourceContainerName</span></span>
<span data-ttu-id="7ea9f-123">Określa nazwę kontenera źródłowego kopii zapasowej w usłudze Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="7ea9f-123">Specifies the name of the Azure storage backup source container.</span></span>

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

### <span data-ttu-id="7ea9f-124">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="7ea9f-124">-StorageContext</span></span>
<span data-ttu-id="7ea9f-125">Określa kontekst połączenia magazynu.</span><span class="sxs-lookup"><span data-stu-id="7ea9f-125">Specifies the storage connection context.</span></span>

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

### <span data-ttu-id="7ea9f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ea9f-126">CommonParameters</span></span>
<span data-ttu-id="7ea9f-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ea9f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ea9f-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ea9f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ea9f-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7ea9f-129">INPUTS</span></span>

### <span data-ttu-id="7ea9f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="7ea9f-130">System.String</span></span>

## <span data-ttu-id="7ea9f-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7ea9f-131">OUTPUTS</span></span>

### <span data-ttu-id="7ea9f-132">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="7ea9f-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="7ea9f-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7ea9f-133">NOTES</span></span>

## <span data-ttu-id="7ea9f-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7ea9f-134">RELATED LINKS</span></span>

[<span data-ttu-id="7ea9f-135">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="7ea9f-135">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="7ea9f-136">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="7ea9f-136">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="7ea9f-137">Nowe — AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="7ea9f-137">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="7ea9f-138">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="7ea9f-138">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)


