---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5846BBB7-DA8E-41B5-A894-BA2B61C2212C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/backup-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Backup-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Backup-AzureRmApiManagement.md
ms.openlocfilehash: d8f243b0b02d724a3979b8c8f318be8e58623cf5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550412"
---
# <span data-ttu-id="3b3ad-101">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="3b3ad-101">Backup-AzureRmApiManagement</span></span>

## <span data-ttu-id="3b3ad-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3b3ad-102">SYNOPSIS</span></span>
<span data-ttu-id="3b3ad-103">Wykonywanie kopii zapasowej usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="3b3ad-103">Backs up an API Management service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b3ad-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3b3ad-104">SYNTAX</span></span>

```
Backup-AzureRmApiManagement -ResourceGroupName <String> -Name <String> -StorageContext <IStorageContext>
 -TargetContainerName <String> [-TargetBlobName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b3ad-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3b3ad-105">DESCRIPTION</span></span>
<span data-ttu-id="3b3ad-106">Polecenie cmdlet **Backup-AzureRmApiManagement** wykonuje kopię zapasową wystąpienia usługi zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="3b3ad-106">The **Backup-AzureRmApiManagement** cmdlet backs up an instance of an Azure API Management service.</span></span>
<span data-ttu-id="3b3ad-107">To polecenie cmdlet zapisuje kopię zapasową jako obiekt BLOB usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="3b3ad-107">This cmdlet stores the backup as an Azure Storage blob.</span></span>

## <span data-ttu-id="3b3ad-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3b3ad-108">EXAMPLES</span></span>

### <span data-ttu-id="3b3ad-109">Przykład 1: wykonywanie kopii zapasowej usługi zarządzania interfejsem API</span><span class="sxs-lookup"><span data-stu-id="3b3ad-109">Example 1: Back up an API Management service</span></span>
```
PS C:\>New-AzureRmStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzureRmStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzureStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Backup-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -StorageContext $StorageContext -TargetContainerName "ContosoBackups" -TargetBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="3b3ad-110">To polecenie wykonuje kopię zapasową usługi zarządzania interfejsem API w obiekcie blob magazynu.</span><span class="sxs-lookup"><span data-stu-id="3b3ad-110">This command backs up an API Management service to a Storage blob.</span></span>

## <span data-ttu-id="3b3ad-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3b3ad-111">PARAMETERS</span></span>

### <span data-ttu-id="3b3ad-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b3ad-112">-DefaultProfile</span></span>
<span data-ttu-id="3b3ad-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3b3ad-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b3ad-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3b3ad-114">-Name</span></span>
<span data-ttu-id="3b3ad-115">Określa nazwę wdrożenia zarządzania interfejsem API, które wykonuje kopia zapasowa tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b3ad-115">Specifies the name of the API Management deployment that this cmdlet backs up.</span></span>

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

### <span data-ttu-id="3b3ad-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3b3ad-116">-PassThru</span></span>
<span data-ttu-id="3b3ad-117">Wskazuje, że to polecenie cmdlet zwróci kopię zapasową obiektu **PsApiManagement** , jeśli operacja się powiedzie.</span><span class="sxs-lookup"><span data-stu-id="3b3ad-117">Indicates that this cmdlet returns the backed up **PsApiManagement** object, if the operation succeeds.</span></span>

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

### <span data-ttu-id="3b3ad-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b3ad-118">-ResourceGroupName</span></span>
<span data-ttu-id="3b3ad-119">Określa nazwę grupy zasobów, w której istnieje wdrożenie zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="3b3ad-119">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="3b3ad-120">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="3b3ad-120">-StorageContext</span></span>
<span data-ttu-id="3b3ad-121">Określa kontekst połączenia magazynu.</span><span class="sxs-lookup"><span data-stu-id="3b3ad-121">Specifies a storage connection context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b3ad-122">-TargetBlobName</span><span class="sxs-lookup"><span data-stu-id="3b3ad-122">-TargetBlobName</span></span>
<span data-ttu-id="3b3ad-123">Określa nazwę obiektu BLOB kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="3b3ad-123">Specifies the name of the blob for the backup.</span></span>
<span data-ttu-id="3b3ad-124">Jeśli obiekt BLOB nie istnieje, to polecenie cmdlet tworzy je.</span><span class="sxs-lookup"><span data-stu-id="3b3ad-124">If the blob does not exist, this cmdlet creates it.</span></span>
<span data-ttu-id="3b3ad-125">To polecenie cmdlet generuje wartość domyślną na podstawie następującego wzorca: {Name}-{RRRR-MM-DD-HH-mm}. apimbackup</span><span class="sxs-lookup"><span data-stu-id="3b3ad-125">This cmdlet generates a default value based on the following pattern: {Name}-{yyyy-MM-dd-HH-mm}.apimbackup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3ad-126">-TargetContainerName</span><span class="sxs-lookup"><span data-stu-id="3b3ad-126">-TargetContainerName</span></span>
<span data-ttu-id="3b3ad-127">Określa nazwę kontenera obiektu BLOB dla kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="3b3ad-127">Specifies the name of the container of the blob for the backup.</span></span>
<span data-ttu-id="3b3ad-128">Jeśli kontener nie istnieje, to polecenie cmdlet utworzy je.</span><span class="sxs-lookup"><span data-stu-id="3b3ad-128">If the container does not exist, this cmdlet creates it.</span></span>

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

### <span data-ttu-id="3b3ad-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b3ad-129">CommonParameters</span></span>
<span data-ttu-id="3b3ad-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b3ad-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b3ad-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b3ad-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b3ad-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3b3ad-132">INPUTS</span></span>

### <span data-ttu-id="3b3ad-133">System. String</span><span class="sxs-lookup"><span data-stu-id="3b3ad-133">System.String</span></span>

### <span data-ttu-id="3b3ad-134">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3b3ad-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3b3ad-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3b3ad-135">OUTPUTS</span></span>

### <span data-ttu-id="3b3ad-136">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="3b3ad-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="3b3ad-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3b3ad-137">NOTES</span></span>

## <span data-ttu-id="3b3ad-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3b3ad-138">RELATED LINKS</span></span>

[<span data-ttu-id="3b3ad-139">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="3b3ad-139">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="3b3ad-140">Nowe — AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="3b3ad-140">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="3b3ad-141">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="3b3ad-141">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="3b3ad-142">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="3b3ad-142">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


