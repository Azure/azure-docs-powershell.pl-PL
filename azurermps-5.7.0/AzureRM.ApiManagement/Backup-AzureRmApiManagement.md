---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: 5846BBB7-DA8E-41B5-A894-BA2B61C2212C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/backup-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Backup-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Backup-AzureRmApiManagement.md
ms.openlocfilehash: 0fd004cdb727a0e665fd9b867854b3b8e4054c9d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719602"
---
# <span data-ttu-id="65431-101">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="65431-101">Backup-AzureRmApiManagement</span></span>

## <span data-ttu-id="65431-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="65431-102">SYNOPSIS</span></span>
<span data-ttu-id="65431-103">Wykonywanie kopii zapasowej usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="65431-103">Backs up an API Management service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65431-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="65431-104">SYNTAX</span></span>

```
Backup-AzureRmApiManagement -ResourceGroupName <String> -Name <String> -StorageContext <IStorageContext>
 -TargetContainerName <String> [-TargetBlobName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65431-105">Opis</span><span class="sxs-lookup"><span data-stu-id="65431-105">DESCRIPTION</span></span>
<span data-ttu-id="65431-106">Polecenie cmdlet **Backup-AzureRmApiManagement** wykonuje kopię zapasową wystąpienia usługi zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="65431-106">The **Backup-AzureRmApiManagement** cmdlet backs up an instance of an Azure API Management service.</span></span>
<span data-ttu-id="65431-107">To polecenie cmdlet zapisuje kopię zapasową jako obiekt BLOB usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="65431-107">This cmdlet stores the backup as an Azure Storage blob.</span></span>

## <span data-ttu-id="65431-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="65431-108">EXAMPLES</span></span>

### <span data-ttu-id="65431-109">Przykład 1: wykonywanie kopii zapasowej usługi zarządzania interfejsem API</span><span class="sxs-lookup"><span data-stu-id="65431-109">Example 1: Back up an API Management service</span></span>
```
PS C:\>New-AzureRmStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzureRmStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzureStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Backup-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -StorageContext $StorageContext -TargetContainerName "ContosoBackups" -TargetBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="65431-110">To polecenie wykonuje kopię zapasową usługi zarządzania interfejsem API w obiekcie blob magazynu.</span><span class="sxs-lookup"><span data-stu-id="65431-110">This command backs up an API Management service to a Storage blob.</span></span>

## <span data-ttu-id="65431-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="65431-111">PARAMETERS</span></span>

### <span data-ttu-id="65431-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65431-112">-DefaultProfile</span></span>
<span data-ttu-id="65431-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="65431-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65431-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="65431-114">-Name</span></span>
<span data-ttu-id="65431-115">Określa nazwę wdrożenia zarządzania interfejsem API, które wykonuje kopia zapasowa tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65431-115">Specifies the name of the API Management deployment that this cmdlet backs up.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65431-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="65431-116">-PassThru</span></span>
<span data-ttu-id="65431-117">Wskazuje, że to polecenie cmdlet zwróci kopię zapasową obiektu **PsApiManagement** , jeśli operacja się powiedzie.</span><span class="sxs-lookup"><span data-stu-id="65431-117">Indicates that this cmdlet returns the backed up **PsApiManagement** object, if the operation succeeds.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65431-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65431-118">-ResourceGroupName</span></span>
<span data-ttu-id="65431-119">Określa nazwę grupy zasobów, w której istnieje wdrożenie zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="65431-119">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65431-120">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="65431-120">-StorageContext</span></span>
<span data-ttu-id="65431-121">Określa kontekst połączenia magazynu.</span><span class="sxs-lookup"><span data-stu-id="65431-121">Specifies a storage connection context.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65431-122">-TargetBlobName</span><span class="sxs-lookup"><span data-stu-id="65431-122">-TargetBlobName</span></span>
<span data-ttu-id="65431-123">Określa nazwę obiektu BLOB kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="65431-123">Specifies the name of the blob for the backup.</span></span>
<span data-ttu-id="65431-124">Jeśli obiekt BLOB nie istnieje, to polecenie cmdlet tworzy je.</span><span class="sxs-lookup"><span data-stu-id="65431-124">If the blob does not exist, this cmdlet creates it.</span></span>
<span data-ttu-id="65431-125">To polecenie cmdlet generuje wartość domyślną na podstawie następującego wzorca:</span><span class="sxs-lookup"><span data-stu-id="65431-125">This cmdlet generates a default value based on the following pattern:</span></span> 

<span data-ttu-id="65431-126">{Name}-{RRRR-MM-DD-HH-mm}. apimbackup</span><span class="sxs-lookup"><span data-stu-id="65431-126">{Name}-{yyyy-MM-dd-HH-mm}.apimbackup</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65431-127">-TargetContainerName</span><span class="sxs-lookup"><span data-stu-id="65431-127">-TargetContainerName</span></span>
<span data-ttu-id="65431-128">Określa nazwę kontenera obiektu BLOB dla kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="65431-128">Specifies the name of the container of the blob for the backup.</span></span>
<span data-ttu-id="65431-129">Jeśli kontener nie istnieje, to polecenie cmdlet utworzy je.</span><span class="sxs-lookup"><span data-stu-id="65431-129">If the container does not exist, this cmdlet creates it.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65431-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65431-130">CommonParameters</span></span>
<span data-ttu-id="65431-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65431-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65431-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65431-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65431-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="65431-133">INPUTS</span></span>

### <span data-ttu-id="65431-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="65431-134">None</span></span>
<span data-ttu-id="65431-135">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="65431-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="65431-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="65431-136">OUTPUTS</span></span>

### <span data-ttu-id="65431-137">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="65431-137">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="65431-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="65431-138">NOTES</span></span>

## <span data-ttu-id="65431-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="65431-139">RELATED LINKS</span></span>

[<span data-ttu-id="65431-140">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="65431-140">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="65431-141">Nowe — AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="65431-141">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="65431-142">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="65431-142">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="65431-143">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="65431-143">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


