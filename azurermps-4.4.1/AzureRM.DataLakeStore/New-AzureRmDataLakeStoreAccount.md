---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 58AAA284-45A3-4360-B321-FBE0A3F5D7A9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: b05cb9e3789afa905da93642929f65f4965f9b0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719653"
---
# <span data-ttu-id="5f6f9-101">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5f6f9-101">New-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="5f6f9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5f6f9-102">SYNOPSIS</span></span>
<span data-ttu-id="5f6f9-103">Tworzy nowe konto w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5f6f9-103">Creates a new Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f6f9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5f6f9-104">SYNTAX</span></span>

### <span data-ttu-id="5f6f9-105">Szyfrowanie przypisane użytkownikowi lub systemowi (domyślne)</span><span class="sxs-lookup"><span data-stu-id="5f6f9-105">User or System assigned encryption (Default)</span></span>
```
New-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tags] <Hashtable>] [[-Encryption] <EncryptionConfigType>]
 [[-KeyVaultId] <String>] [[-KeyName] <String>] [[-KeyVersion] <String>] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f6f9-106">Wyłączanie szyfrowania</span><span class="sxs-lookup"><span data-stu-id="5f6f9-106">Disable Encryption</span></span>
```
New-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tags] <Hashtable>] [-DisableEncryption] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f6f9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="5f6f9-107">DESCRIPTION</span></span>
<span data-ttu-id="5f6f9-108">Polecenie cmdlet **New-AzureRmDataLakeStoreAccount** tworzy nowe konto usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5f6f9-108">The **New-AzureRmDataLakeStoreAccount** cmdlet creates a new Data Lake Store account.</span></span>

## <span data-ttu-id="5f6f9-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5f6f9-109">EXAMPLES</span></span>

### <span data-ttu-id="5f6f9-110">Przykład 1. Tworzenie konta</span><span class="sxs-lookup"><span data-stu-id="5f6f9-110">Example 1: Create an account</span></span>
```
PS C:\>New-AzureRmDataLakeStoreAccount -Name "ContosoADL" -ResourceGroupName "ContosoOrg" -Location "East US 2"
```

<span data-ttu-id="5f6f9-111">To polecenie tworzy konto usługi Data Lake Store o nazwie ContosoADL dla pozycji wschód w Stanach Zjednoczonych 2.</span><span class="sxs-lookup"><span data-stu-id="5f6f9-111">This command creates a Data Lake Store account named ContosoADL for the East US 2 location.</span></span>

## <span data-ttu-id="5f6f9-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5f6f9-112">PARAMETERS</span></span>

### <span data-ttu-id="5f6f9-113">-Domyślna</span><span class="sxs-lookup"><span data-stu-id="5f6f9-113">-DefaultGroup</span></span>
<span data-ttu-id="5f6f9-114">Określa identyfikator obiektu katalogu AzureActive, który ma być używany jako domyślny właściciel grupy dla nowych plików i folderów.</span><span class="sxs-lookup"><span data-stu-id="5f6f9-114">Specifies the object ID of the AzureActive Directory group to use as the default group owner for new files and folders.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f6f9-115">-DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="5f6f9-115">-DisableEncryption</span></span>
<span data-ttu-id="5f6f9-116">Wskazuje, że do konta nie zastosowano żadnej formy szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="5f6f9-116">Indicates that the account will not have any form of encryption applied to it.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable Encryption
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f6f9-117">— Szyfrowanie</span><span class="sxs-lookup"><span data-stu-id="5f6f9-117">-Encryption</span></span>
```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.EncryptionConfigType]
Parameter Sets: User or System assigned encryption
Aliases: 
Accepted values: UserManaged, ServiceManaged

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f6f9-118">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="5f6f9-118">-KeyName</span></span>
```yaml
Type: System.String
Parameter Sets: User or System assigned encryption
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f6f9-119">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="5f6f9-119">-KeyVaultId</span></span>
```yaml
Type: System.String
Parameter Sets: User or System assigned encryption
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f6f9-120">-Wersja-</span><span class="sxs-lookup"><span data-stu-id="5f6f9-120">-KeyVersion</span></span>
```yaml
Type: System.String
Parameter Sets: User or System assigned encryption
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f6f9-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="5f6f9-121">-Location</span></span>
<span data-ttu-id="5f6f9-122">Określa lokalizację, w której ma być używane konto.</span><span class="sxs-lookup"><span data-stu-id="5f6f9-122">Specifies the location to use for the account.</span></span>
<span data-ttu-id="5f6f9-123">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="5f6f9-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5f6f9-124">Wschód USA 2</span><span class="sxs-lookup"><span data-stu-id="5f6f9-124">East US 2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f6f9-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5f6f9-125">-Name</span></span>
<span data-ttu-id="5f6f9-126">Określa nazwę konta, które ma zostać utworzone.</span><span class="sxs-lookup"><span data-stu-id="5f6f9-126">Specifies the name of the account to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f6f9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f6f9-127">-ResourceGroupName</span></span>
<span data-ttu-id="5f6f9-128">Określa nazwę grupy zasobów zawierającej dane konto.</span><span class="sxs-lookup"><span data-stu-id="5f6f9-128">Specifies the name of the resource group that contains the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f6f9-129">-Tagi</span><span class="sxs-lookup"><span data-stu-id="5f6f9-129">-Tags</span></span>
<span data-ttu-id="5f6f9-130">Określa znaczniki jako pary klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="5f6f9-130">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="5f6f9-131">Za pomocą znaczników możesz identyfikować konta usługi Data Lake Store z innych zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5f6f9-131">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f6f9-132">-Warstwowy</span><span class="sxs-lookup"><span data-stu-id="5f6f9-132">-Tier</span></span>
<span data-ttu-id="5f6f9-133">Pożądana warstwa zobowiązań do użycia dla tego konta.</span><span class="sxs-lookup"><span data-stu-id="5f6f9-133">The desired commitment tier for this account to use.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.TierType]
Parameter Sets: (All)
Aliases: 
Accepted values: Consumption, Commitment1TB, Commitment10TB, Commitment100TB, Commitment500TB, Commitment1PB, Commitment5PB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f6f9-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f6f9-134">-DefaultProfile</span></span>
<span data-ttu-id="5f6f9-135">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5f6f9-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f6f9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f6f9-136">CommonParameters</span></span>
<span data-ttu-id="5f6f9-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f6f9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f6f9-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f6f9-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f6f9-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5f6f9-139">INPUTS</span></span>

## <span data-ttu-id="5f6f9-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5f6f9-140">OUTPUTS</span></span>

### <span data-ttu-id="5f6f9-141">PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5f6f9-141">PSDataLakeStoreAccount</span></span>
<span data-ttu-id="5f6f9-142">Utworzone dane konta.</span><span class="sxs-lookup"><span data-stu-id="5f6f9-142">The created account details.</span></span>

## <span data-ttu-id="5f6f9-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5f6f9-143">NOTES</span></span>

## <span data-ttu-id="5f6f9-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5f6f9-144">RELATED LINKS</span></span>

[<span data-ttu-id="5f6f9-145">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5f6f9-145">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="5f6f9-146">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5f6f9-146">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="5f6f9-147">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5f6f9-147">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="5f6f9-148">Test — AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5f6f9-148">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


