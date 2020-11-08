---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: BF054CA4-B0A4-4BFC-A657-92A0D3ABBCB5
online version: ''
schema: 2.0.0
ms.openlocfilehash: f82db6a826a6ed612e1d98c7cef6ab642bf15858
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054517"
---
# <span data-ttu-id="b77ce-101">Get-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="b77ce-101">Get-AzureStorSimpleStorageAccountCredential</span></span>

## <span data-ttu-id="b77ce-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b77ce-102">SYNOPSIS</span></span>
<span data-ttu-id="b77ce-103">Pobiera poświadczenia kont magazynu.</span><span class="sxs-lookup"><span data-stu-id="b77ce-103">Gets credentials for storage accounts.</span></span>

## <span data-ttu-id="b77ce-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b77ce-104">SYNTAX</span></span>

```
Get-AzureStorSimpleStorageAccountCredential [-StorageAccountName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="b77ce-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b77ce-105">DESCRIPTION</span></span>
<span data-ttu-id="b77ce-106">Polecenie cmdlet **Get-AzureStorSimpleStorageAccountCredential** Pobiera poświadczenia kont magazynu.</span><span class="sxs-lookup"><span data-stu-id="b77ce-106">The **Get-AzureStorSimpleStorageAccountCredential** cmdlet gets credentials for storage accounts.</span></span>
<span data-ttu-id="b77ce-107">To polecenie cmdlet umożliwia pobieranie wszystkich obiektów **StorageAccountCredential** skonfigurowanych w usłudze lub nazwanego **StorageAccountCredential**.</span><span class="sxs-lookup"><span data-stu-id="b77ce-107">This cmdlet gets all **StorageAccountCredential** objects configured in the service or a named **StorageAccountCredential**.</span></span>

## <span data-ttu-id="b77ce-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b77ce-108">EXAMPLES</span></span>

### <span data-ttu-id="b77ce-109">Przykład 1. pobieranie wszystkich poświadczeń dla zasobu</span><span class="sxs-lookup"><span data-stu-id="b77ce-109">Example 1: Get all credentials for a resource</span></span>
```
PS C:\>Get-AzureStorSimpleStorageAccountCredential
InstanceId                           Login           Name            UseSSL VolumeCount     CloudType    Location
----------                           -----           ----            ------ -----------     ---------    --------
b5e0857f-82ef-4426-883b-a612889ebee4 qwertyuiopa     AdminAccount    True   24              Azure
```

<span data-ttu-id="b77ce-110">To polecenie pobiera wszystkie dostępne poświadczenia kont magazynu dla bieżącego zasobu.</span><span class="sxs-lookup"><span data-stu-id="b77ce-110">This command gets all available credentials for storage accounts for the current resource.</span></span>

### <span data-ttu-id="b77ce-111">Przykład 2: uzyskiwanie poświadczenia dla określonego konta magazynu</span><span class="sxs-lookup"><span data-stu-id="b77ce-111">Example 2: Get the credential for a specific storage account</span></span>
```
PS C:\>Get-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoCloudStorage"
VERBOSE: ClientRequestId: 16551af6-3398-4d30-a389-1b8eb01ce92c_PS
VERBOSE: ClientRequestId: 5041277d-4044-4b6c-ae19-4ea9e7ae135a_PS
VERBOSE: Storage Access Credential with name ContosoCloudStorage found! 


CloudType                        : Azure
Hostname                         : blob.core.windows.net
InstanceId                       : 8b3cb7bb-963b-4173-9598-52fe230b0350
IsDefault                        : False
Location                         : West US
Login                            : ContosoCloudStorage
Name                             : ContosoCloudStorage
OperationInProgress              : None
Password                         : 
PasswordEncryptionCertThumbprint : 
UseSSL                           : True
VolumeCount                      : 0
```

<span data-ttu-id="b77ce-112">To polecenie pobiera poświadczenia konta magazynu dla konta magazynu o nazwie ContosoCloudStorage.</span><span class="sxs-lookup"><span data-stu-id="b77ce-112">This command gets the storage account credential for the storage account named ContosoCloudStorage.</span></span>

## <span data-ttu-id="b77ce-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b77ce-113">PARAMETERS</span></span>

### <span data-ttu-id="b77ce-114">-Profile</span><span class="sxs-lookup"><span data-stu-id="b77ce-114">-Profile</span></span>
<span data-ttu-id="b77ce-115">Określa Profil platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b77ce-115">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b77ce-116">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b77ce-116">-StorageAccountName</span></span>
<span data-ttu-id="b77ce-117">Określa nazwę konta magazynu, dla którego mają być uzyskiwane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="b77ce-117">Specifies the name of the storage account for which to get credentials.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b77ce-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b77ce-118">CommonParameters</span></span>
<span data-ttu-id="b77ce-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b77ce-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b77ce-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b77ce-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b77ce-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b77ce-121">INPUTS</span></span>

### <span data-ttu-id="b77ce-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b77ce-122">None</span></span>

## <span data-ttu-id="b77ce-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b77ce-123">OUTPUTS</span></span>

### <span data-ttu-id="b77ce-124">StorageAccountCredential, IList\<StorageAccountCredential\></span><span class="sxs-lookup"><span data-stu-id="b77ce-124">StorageAccountCredential, IList\<StorageAccountCredential\></span></span>
<span data-ttu-id="b77ce-125">To polecenie cmdlet zwraca obiekt **StorageAccountCredential** , jeśli określisz parametr *StorageAccountName* lub nie określisz tego parametru, zwraca obiekt **IList \<StorageAccountCredential\>** .</span><span class="sxs-lookup"><span data-stu-id="b77ce-125">This cmdlet returns a **StorageAccountCredential** object, if you specify the *StorageAccountName* parameter, or if you do not specify that parameter, it returns an **IList\<StorageAccountCredential\>** object.</span></span>

## <span data-ttu-id="b77ce-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b77ce-126">NOTES</span></span>

## <span data-ttu-id="b77ce-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b77ce-127">RELATED LINKS</span></span>

[<span data-ttu-id="b77ce-128">Nowe — AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="b77ce-128">New-AzureStorSimpleStorageAccountCredential</span></span>](./New-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="b77ce-129">Remove-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="b77ce-129">Remove-AzureStorSimpleStorageAccountCredential</span></span>](./Remove-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="b77ce-130">Set-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="b77ce-130">Set-AzureStorSimpleStorageAccountCredential</span></span>](./Set-AzureStorSimpleStorageAccountCredential.md)


