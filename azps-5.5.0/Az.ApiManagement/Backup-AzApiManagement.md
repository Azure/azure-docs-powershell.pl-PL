---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5846BBB7-DA8E-41B5-A894-BA2B61C2212C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/backup-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Backup-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Backup-AzApiManagement.md
ms.openlocfilehash: fcdd498c99c10857e0fa76c890bc6be6e9733b84
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187770"
---
# <span data-ttu-id="27556-101">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="27556-101">Backup-AzApiManagement</span></span>

## <span data-ttu-id="27556-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27556-102">SYNOPSIS</span></span>
<span data-ttu-id="27556-103">Umożliwia kopię zapasową usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="27556-103">Backs up an API Management service.</span></span>

## <span data-ttu-id="27556-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="27556-104">SYNTAX</span></span>

```
Backup-AzApiManagement -ResourceGroupName <String> -Name <String> -StorageContext <IStorageContext>
 -TargetContainerName <String> [-TargetBlobName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27556-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="27556-105">DESCRIPTION</span></span>
<span data-ttu-id="27556-106">Polecenie **cmdlet Backup-AzApiManagement** umożliwia tworzenie kopii zapasowej wystąpienia usługi Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="27556-106">The **Backup-AzApiManagement** cmdlet backs up an instance of an Azure API Management service.</span></span>
<span data-ttu-id="27556-107">To polecenie cmdlet przechowuje kopię zapasową jako obiekt blob magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="27556-107">This cmdlet stores the backup as an Azure Storage blob.</span></span>

## <span data-ttu-id="27556-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="27556-108">EXAMPLES</span></span>

### <span data-ttu-id="27556-109">Przykład 1. Kopii zapasowej usługi zarządzania interfejsem API</span><span class="sxs-lookup"><span data-stu-id="27556-109">Example 1: Back up an API Management service</span></span>
```
PS C:\>New-AzStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Backup-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -StorageContext $StorageContext -TargetContainerName "ContosoBackups" -TargetBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="27556-110">To polecenie umożliwia kopię zapasową usługi zarządzania interfejsem API w obiekcie blob magazynu.</span><span class="sxs-lookup"><span data-stu-id="27556-110">This command backs up an API Management service to a Storage blob.</span></span>

## <span data-ttu-id="27556-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27556-111">PARAMETERS</span></span>

### <span data-ttu-id="27556-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27556-112">-DefaultProfile</span></span>
<span data-ttu-id="27556-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="27556-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27556-114">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="27556-114">-Name</span></span>
<span data-ttu-id="27556-115">Określa nazwę wdrożenia zarządzania interfejsami API, dla których to polecenie cmdlet ma być kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="27556-115">Specifies the name of the API Management deployment that this cmdlet backs up.</span></span>

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

### <span data-ttu-id="27556-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="27556-116">-PassThru</span></span>
<span data-ttu-id="27556-117">Wskazuje, że to polecenie cmdlet zwraca kopię zapasową obiektu **PsApiManagement,** jeśli operacja się powiedzie.</span><span class="sxs-lookup"><span data-stu-id="27556-117">Indicates that this cmdlet returns the backed up **PsApiManagement** object, if the operation succeeds.</span></span>

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

### <span data-ttu-id="27556-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27556-118">-ResourceGroupName</span></span>
<span data-ttu-id="27556-119">Określa nazwę grupy zasobów, w ramach której istnieje wdrożenie zarządzanie interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="27556-119">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="27556-120">- StorageContext</span><span class="sxs-lookup"><span data-stu-id="27556-120">-StorageContext</span></span>
<span data-ttu-id="27556-121">Określa kontekst połączenia magazynu.</span><span class="sxs-lookup"><span data-stu-id="27556-121">Specifies a storage connection context.</span></span>

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

### <span data-ttu-id="27556-122">-TargetBlobName</span><span class="sxs-lookup"><span data-stu-id="27556-122">-TargetBlobName</span></span>
<span data-ttu-id="27556-123">Określa nazwę obiektu blob dla kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="27556-123">Specifies the name of the blob for the backup.</span></span>
<span data-ttu-id="27556-124">Jeśli obiekt blob nie istnieje, to polecenie cmdlet utworzy go.</span><span class="sxs-lookup"><span data-stu-id="27556-124">If the blob does not exist, this cmdlet creates it.</span></span>
<span data-ttu-id="27556-125">To polecenie cmdlet generuje wartość domyślną na podstawie następującego wzorca: {Name}-{yyyy-MM-dd-HH-mm}.apimbackup</span><span class="sxs-lookup"><span data-stu-id="27556-125">This cmdlet generates a default value based on the following pattern: {Name}-{yyyy-MM-dd-HH-mm}.apimbackup</span></span>

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

### <span data-ttu-id="27556-126">-TargetContainerName</span><span class="sxs-lookup"><span data-stu-id="27556-126">-TargetContainerName</span></span>
<span data-ttu-id="27556-127">Określa nazwę kontenera obiektu blob dla kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="27556-127">Specifies the name of the container of the blob for the backup.</span></span>
<span data-ttu-id="27556-128">Jeśli kontener nie istnieje, to polecenie cmdlet go utworzy.</span><span class="sxs-lookup"><span data-stu-id="27556-128">If the container does not exist, this cmdlet creates it.</span></span>

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

### <span data-ttu-id="27556-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27556-129">CommonParameters</span></span>
<span data-ttu-id="27556-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27556-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27556-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="27556-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27556-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="27556-132">INPUTS</span></span>

### <span data-ttu-id="27556-133">System.String</span><span class="sxs-lookup"><span data-stu-id="27556-133">System.String</span></span>

### <span data-ttu-id="27556-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="27556-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="27556-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="27556-135">OUTPUTS</span></span>

### <span data-ttu-id="27556-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="27556-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="27556-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="27556-137">NOTES</span></span>

## <span data-ttu-id="27556-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="27556-138">RELATED LINKS</span></span>

[<span data-ttu-id="27556-139">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="27556-139">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="27556-140">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="27556-140">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="27556-141">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="27556-141">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="27556-142">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="27556-142">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


