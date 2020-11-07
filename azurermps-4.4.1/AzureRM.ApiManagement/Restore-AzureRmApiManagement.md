---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 022BBF5F-AFF1-45D5-9153-872779FFBAF4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Restore-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Restore-AzureRmApiManagement.md
ms.openlocfilehash: 9e19d8e205010ce55886761d2cbb7fd904d5277d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716546"
---
# <span data-ttu-id="b9ea9-101">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="b9ea9-101">Restore-AzureRmApiManagement</span></span>

## <span data-ttu-id="b9ea9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b9ea9-102">SYNOPSIS</span></span>
<span data-ttu-id="b9ea9-103">Przywraca usługę zarządzania interfejsem API z określonego obiektu blob magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b9ea9-103">Restores an API Management Service from the specified Azure storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9ea9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b9ea9-104">SYNTAX</span></span>

```
Restore-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-StorageContext] <IStorageContext>
 -SourceContainerName <String> -SourceBlobName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b9ea9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b9ea9-105">DESCRIPTION</span></span>
<span data-ttu-id="b9ea9-106">Polecenie cmdlet **Restore-AzureRmApiManagement** przywraca usługę zarządzania interfejsem API z określonej kopii zapasowej znajdującej się w obiekcie blob Azurestorage.</span><span class="sxs-lookup"><span data-stu-id="b9ea9-106">The **Restore-AzureRmApiManagement** cmdlet restores an API Management Service from the specified backup residing in an Azurestorage blob.</span></span>

## <span data-ttu-id="b9ea9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b9ea9-107">EXAMPLES</span></span>

### <span data-ttu-id="b9ea9-108">Przykład 1: Przywracanie usługi zarządzania interfejsem API</span><span class="sxs-lookup"><span data-stu-id="b9ea9-108">Example 1: Restore an API Management service</span></span>
```
PS C:\>Restore-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "RestoredContosoApi" -StorageContext $StorageContext -SourceContainerName "ContosoBackups" -SourceBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="b9ea9-109">To polecenie przywraca usługę zarządzania interfejsem API z obiektu blob magazynu Azure.</span><span class="sxs-lookup"><span data-stu-id="b9ea9-109">This command restores an API Management service from Azure storage blob.</span></span>

## <span data-ttu-id="b9ea9-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b9ea9-110">PARAMETERS</span></span>

### <span data-ttu-id="b9ea9-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b9ea9-111">-Name</span></span>
<span data-ttu-id="b9ea9-112">Określa nazwę wystąpienia zarządzania interfejsem API, które zostanie przywrócone przy użyciu kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="b9ea9-112">Specifies the name of the API Management instance that will be restored with the backup.</span></span>

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

### <span data-ttu-id="b9ea9-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b9ea9-113">-PassThru</span></span>
<span data-ttu-id="b9ea9-114">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="b9ea9-114">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b9ea9-115">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="b9ea9-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b9ea9-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9ea9-116">-ResourceGroupName</span></span>
<span data-ttu-id="b9ea9-117">Określa nazwę grupy zasobów, pod którą istnieje zarządzanie interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="b9ea9-117">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="b9ea9-118">-SourceBlobName</span><span class="sxs-lookup"><span data-stu-id="b9ea9-118">-SourceBlobName</span></span>
<span data-ttu-id="b9ea9-119">Określa nazwę obiektu BLOB źródła kopii zapasowej Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="b9ea9-119">Specifies the name of the Azure storage backup source blob.</span></span>

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

### <span data-ttu-id="b9ea9-120">-SourceContainerName</span><span class="sxs-lookup"><span data-stu-id="b9ea9-120">-SourceContainerName</span></span>
<span data-ttu-id="b9ea9-121">Określa nazwę kontenera źródłowego kopii zapasowej w usłudze Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="b9ea9-121">Specifies the name of the Azure storage backup source container.</span></span>

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

### <span data-ttu-id="b9ea9-122">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="b9ea9-122">-StorageContext</span></span>
<span data-ttu-id="b9ea9-123">Określa kontekst połączenia magazynu.</span><span class="sxs-lookup"><span data-stu-id="b9ea9-123">Specifies the storage connection context.</span></span>

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

### <span data-ttu-id="b9ea9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9ea9-124">-DefaultProfile</span></span>
<span data-ttu-id="b9ea9-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b9ea9-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9ea9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9ea9-126">CommonParameters</span></span>
<span data-ttu-id="b9ea9-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9ea9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9ea9-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9ea9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9ea9-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b9ea9-129">INPUTS</span></span>

## <span data-ttu-id="b9ea9-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b9ea9-130">OUTPUTS</span></span>

### <span data-ttu-id="b9ea9-131">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="b9ea9-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="b9ea9-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b9ea9-132">NOTES</span></span>

## <span data-ttu-id="b9ea9-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b9ea9-133">RELATED LINKS</span></span>

[<span data-ttu-id="b9ea9-134">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="b9ea9-134">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="b9ea9-135">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="b9ea9-135">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="b9ea9-136">Nowe — AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="b9ea9-136">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="b9ea9-137">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="b9ea9-137">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)


