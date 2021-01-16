---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5846BBB7-DA8E-41B5-A894-BA2B61C2212C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/backup-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Backup-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Backup-AzApiManagement.md
ms.openlocfilehash: fcdd498c99c10857e0fa76c890bc6be6e9733b84
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333154"
---
# <span data-ttu-id="4ebef-101">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="4ebef-101">Backup-AzApiManagement</span></span>

## <span data-ttu-id="4ebef-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4ebef-102">SYNOPSIS</span></span>
<span data-ttu-id="4ebef-103">Wykonywanie kopii zapasowej usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="4ebef-103">Backs up an API Management service.</span></span>

## <span data-ttu-id="4ebef-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4ebef-104">SYNTAX</span></span>

```
Backup-AzApiManagement -ResourceGroupName <String> -Name <String> -StorageContext <IStorageContext>
 -TargetContainerName <String> [-TargetBlobName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ebef-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4ebef-105">DESCRIPTION</span></span>
<span data-ttu-id="4ebef-106">Polecenie cmdlet **Backup-AzApiManagement** wykonuje kopię zapasową wystąpienia usługi zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="4ebef-106">The **Backup-AzApiManagement** cmdlet backs up an instance of an Azure API Management service.</span></span>
<span data-ttu-id="4ebef-107">To polecenie cmdlet zapisuje kopię zapasową jako obiekt BLOB usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="4ebef-107">This cmdlet stores the backup as an Azure Storage blob.</span></span>

## <span data-ttu-id="4ebef-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4ebef-108">EXAMPLES</span></span>

### <span data-ttu-id="4ebef-109">Przykład 1: wykonywanie kopii zapasowej usługi zarządzania interfejsem API</span><span class="sxs-lookup"><span data-stu-id="4ebef-109">Example 1: Back up an API Management service</span></span>
```
PS C:\>New-AzStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Backup-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -StorageContext $StorageContext -TargetContainerName "ContosoBackups" -TargetBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="4ebef-110">To polecenie wykonuje kopię zapasową usługi zarządzania interfejsem API w obiekcie blob magazynu.</span><span class="sxs-lookup"><span data-stu-id="4ebef-110">This command backs up an API Management service to a Storage blob.</span></span>

## <span data-ttu-id="4ebef-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4ebef-111">PARAMETERS</span></span>

### <span data-ttu-id="4ebef-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ebef-112">-DefaultProfile</span></span>
<span data-ttu-id="4ebef-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4ebef-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ebef-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4ebef-114">-Name</span></span>
<span data-ttu-id="4ebef-115">Określa nazwę wdrożenia zarządzania interfejsem API, które wykonuje kopia zapasowa tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ebef-115">Specifies the name of the API Management deployment that this cmdlet backs up.</span></span>

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

### <span data-ttu-id="4ebef-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4ebef-116">-PassThru</span></span>
<span data-ttu-id="4ebef-117">Wskazuje, że to polecenie cmdlet zwróci kopię zapasową obiektu **PsApiManagement** , jeśli operacja się powiedzie.</span><span class="sxs-lookup"><span data-stu-id="4ebef-117">Indicates that this cmdlet returns the backed up **PsApiManagement** object, if the operation succeeds.</span></span>

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

### <span data-ttu-id="4ebef-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ebef-118">-ResourceGroupName</span></span>
<span data-ttu-id="4ebef-119">Określa nazwę grupy zasobów, w której istnieje wdrożenie zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="4ebef-119">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="4ebef-120">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="4ebef-120">-StorageContext</span></span>
<span data-ttu-id="4ebef-121">Określa kontekst połączenia magazynu.</span><span class="sxs-lookup"><span data-stu-id="4ebef-121">Specifies a storage connection context.</span></span>

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

### <span data-ttu-id="4ebef-122">-TargetBlobName</span><span class="sxs-lookup"><span data-stu-id="4ebef-122">-TargetBlobName</span></span>
<span data-ttu-id="4ebef-123">Określa nazwę obiektu BLOB kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="4ebef-123">Specifies the name of the blob for the backup.</span></span>
<span data-ttu-id="4ebef-124">Jeśli obiekt BLOB nie istnieje, to polecenie cmdlet tworzy je.</span><span class="sxs-lookup"><span data-stu-id="4ebef-124">If the blob does not exist, this cmdlet creates it.</span></span>
<span data-ttu-id="4ebef-125">To polecenie cmdlet generuje wartość domyślną na podstawie następującego wzorca: {Name}-{RRRR-MM-DD-HH-mm}. apimbackup</span><span class="sxs-lookup"><span data-stu-id="4ebef-125">This cmdlet generates a default value based on the following pattern: {Name}-{yyyy-MM-dd-HH-mm}.apimbackup</span></span>

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

### <span data-ttu-id="4ebef-126">-TargetContainerName</span><span class="sxs-lookup"><span data-stu-id="4ebef-126">-TargetContainerName</span></span>
<span data-ttu-id="4ebef-127">Określa nazwę kontenera obiektu BLOB dla kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="4ebef-127">Specifies the name of the container of the blob for the backup.</span></span>
<span data-ttu-id="4ebef-128">Jeśli kontener nie istnieje, to polecenie cmdlet utworzy je.</span><span class="sxs-lookup"><span data-stu-id="4ebef-128">If the container does not exist, this cmdlet creates it.</span></span>

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

### <span data-ttu-id="4ebef-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ebef-129">CommonParameters</span></span>
<span data-ttu-id="4ebef-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ebef-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ebef-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4ebef-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ebef-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4ebef-132">INPUTS</span></span>

### <span data-ttu-id="4ebef-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4ebef-133">System.String</span></span>

### <span data-ttu-id="4ebef-134">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4ebef-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4ebef-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4ebef-135">OUTPUTS</span></span>

### <span data-ttu-id="4ebef-136">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="4ebef-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="4ebef-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4ebef-137">NOTES</span></span>

## <span data-ttu-id="4ebef-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4ebef-138">RELATED LINKS</span></span>

[<span data-ttu-id="4ebef-139">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="4ebef-139">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="4ebef-140">Nowe — AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="4ebef-140">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="4ebef-141">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="4ebef-141">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="4ebef-142">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="4ebef-142">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


