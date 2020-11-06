---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 58AAA284-45A3-4360-B321-FBE0A3F5D7A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/new-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: c9964bfb6d9f701d88a16b8a227aec7c2018a217
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526846"
---
# <span data-ttu-id="4df3d-101">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="4df3d-101">New-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="4df3d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4df3d-102">SYNOPSIS</span></span>
<span data-ttu-id="4df3d-103">Tworzy nowe konto w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4df3d-103">Creates a new Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4df3d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4df3d-104">SYNTAX</span></span>

### <span data-ttu-id="4df3d-105">UserOrSystemAssignedEncryption (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4df3d-105">UserOrSystemAssignedEncryption (Default)</span></span>
```
New-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tag] <Hashtable>] [[-Encryption] <EncryptionConfigType>]
 [[-KeyVaultId] <String>] [[-KeyName] <String>] [[-KeyVersion] <String>] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4df3d-106">DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="4df3d-106">DisableEncryption</span></span>
```
New-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tag] <Hashtable>] [-DisableEncryption] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4df3d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4df3d-107">DESCRIPTION</span></span>
<span data-ttu-id="4df3d-108">Polecenie cmdlet **New-AzureRmDataLakeStoreAccount** tworzy nowe konto usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4df3d-108">The **New-AzureRmDataLakeStoreAccount** cmdlet creates a new Data Lake Store account.</span></span>

## <span data-ttu-id="4df3d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4df3d-109">EXAMPLES</span></span>

### <span data-ttu-id="4df3d-110">Przykład 1. Tworzenie konta</span><span class="sxs-lookup"><span data-stu-id="4df3d-110">Example 1: Create an account</span></span>
```
PS C:\>New-AzureRmDataLakeStoreAccount -Name "ContosoADL" -ResourceGroupName "ContosoOrg" -Location "East US 2"
```

<span data-ttu-id="4df3d-111">To polecenie tworzy konto usługi Data Lake Store o nazwie ContosoADL dla pozycji wschód w Stanach Zjednoczonych 2.</span><span class="sxs-lookup"><span data-stu-id="4df3d-111">This command creates a Data Lake Store account named ContosoADL for the East US 2 location.</span></span>

## <span data-ttu-id="4df3d-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4df3d-112">PARAMETERS</span></span>

### <span data-ttu-id="4df3d-113">-Domyślna</span><span class="sxs-lookup"><span data-stu-id="4df3d-113">-DefaultGroup</span></span>
<span data-ttu-id="4df3d-114">Określa identyfikator obiektu katalogu AzureActive, który ma być używany jako domyślny właściciel grupy dla nowych plików i folderów.</span><span class="sxs-lookup"><span data-stu-id="4df3d-114">Specifies the object ID of the AzureActive Directory group to use as the default group owner for new files and folders.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4df3d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4df3d-115">-DefaultProfile</span></span>
<span data-ttu-id="4df3d-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="4df3d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4df3d-117">-DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="4df3d-117">-DisableEncryption</span></span>
<span data-ttu-id="4df3d-118">Wskazuje, że do konta nie zastosowano żadnej formy szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="4df3d-118">Indicates that the account will not have any form of encryption applied to it.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableEncryption
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4df3d-119">— Szyfrowanie</span><span class="sxs-lookup"><span data-stu-id="4df3d-119">-Encryption</span></span>
```yaml
Type: EncryptionConfigType
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:
Accepted values: UserManaged, ServiceManaged

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4df3d-120">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="4df3d-120">-KeyName</span></span>
```yaml
Type: String
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4df3d-121">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="4df3d-121">-KeyVaultId</span></span>
```yaml
Type: String
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4df3d-122">-Wersja-</span><span class="sxs-lookup"><span data-stu-id="4df3d-122">-KeyVersion</span></span>
```yaml
Type: String
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4df3d-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="4df3d-123">-Location</span></span>
<span data-ttu-id="4df3d-124">Określa lokalizację, w której ma być używane konto.</span><span class="sxs-lookup"><span data-stu-id="4df3d-124">Specifies the location to use for the account.</span></span>
<span data-ttu-id="4df3d-125">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="4df3d-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4df3d-126">Wschód USA 2</span><span class="sxs-lookup"><span data-stu-id="4df3d-126">East US 2</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4df3d-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4df3d-127">-Name</span></span>
<span data-ttu-id="4df3d-128">Określa nazwę konta, które ma zostać utworzone.</span><span class="sxs-lookup"><span data-stu-id="4df3d-128">Specifies the name of the account to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4df3d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4df3d-129">-ResourceGroupName</span></span>
<span data-ttu-id="4df3d-130">Określa nazwę grupy zasobów zawierającej dane konto.</span><span class="sxs-lookup"><span data-stu-id="4df3d-130">Specifies the name of the resource group that contains the account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4df3d-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="4df3d-131">-Tag</span></span>
<span data-ttu-id="4df3d-132">Określa znaczniki jako pary klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="4df3d-132">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="4df3d-133">Za pomocą znaczników możesz identyfikować konta usługi Data Lake Store z innych zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4df3d-133">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4df3d-134">-Warstwowy</span><span class="sxs-lookup"><span data-stu-id="4df3d-134">-Tier</span></span>
<span data-ttu-id="4df3d-135">Pożądana warstwa zobowiązań do użycia dla tego konta.</span><span class="sxs-lookup"><span data-stu-id="4df3d-135">The desired commitment tier for this account to use.</span></span>

```yaml
Type: TierType
Parameter Sets: (All)
Aliases:
Accepted values: Consumption, Commitment1TB, Commitment10TB, Commitment100TB, Commitment500TB, Commitment1PB, Commitment5PB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4df3d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4df3d-136">CommonParameters</span></span>
<span data-ttu-id="4df3d-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4df3d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4df3d-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4df3d-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4df3d-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4df3d-139">INPUTS</span></span>

### <span data-ttu-id="4df3d-140">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="4df3d-140">None</span></span>
<span data-ttu-id="4df3d-141">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="4df3d-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4df3d-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4df3d-142">OUTPUTS</span></span>

### <span data-ttu-id="4df3d-143">PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="4df3d-143">PSDataLakeStoreAccount</span></span>
<span data-ttu-id="4df3d-144">Utworzone dane konta.</span><span class="sxs-lookup"><span data-stu-id="4df3d-144">The created account details.</span></span>

## <span data-ttu-id="4df3d-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4df3d-145">NOTES</span></span>

## <span data-ttu-id="4df3d-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4df3d-146">RELATED LINKS</span></span>

[<span data-ttu-id="4df3d-147">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="4df3d-147">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="4df3d-148">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="4df3d-148">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="4df3d-149">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="4df3d-149">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="4df3d-150">Test — AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="4df3d-150">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


