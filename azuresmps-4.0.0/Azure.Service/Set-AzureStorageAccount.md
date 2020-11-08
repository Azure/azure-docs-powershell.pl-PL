---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: EB4A7F84-99E4-49B1-856D-EC0736058D23
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8cab29cd7d285d2ae1aae9c007be965e1bbf8f2f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054816"
---
# <span data-ttu-id="7554a-101">Set-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7554a-101">Set-AzureStorageAccount</span></span>

## <span data-ttu-id="7554a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7554a-102">SYNOPSIS</span></span>
<span data-ttu-id="7554a-103">Aktualizuje właściwości konta magazynu w ramach subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7554a-103">Updates the properties of a storage account in an Azure subscription.</span></span>

## <span data-ttu-id="7554a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7554a-104">SYNTAX</span></span>

### <span data-ttu-id="7554a-105">AccountName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="7554a-105">AccountType (Default)</span></span>
```
Set-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 [-Type <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="7554a-106">GeoReplicationEnabled</span><span class="sxs-lookup"><span data-stu-id="7554a-106">GeoReplicationEnabled</span></span>
```
Set-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 [-GeoReplicationEnabled <Boolean>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="7554a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7554a-107">DESCRIPTION</span></span>
<span data-ttu-id="7554a-108">Polecenie cmdlet **Set-AzureStorageAccount** aktualizuje właściwości konta usługi Azure Storage w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="7554a-108">The **Set-AzureStorageAccount** cmdlet updates the properties of an Azure storage account in the current subscription.</span></span>
<span data-ttu-id="7554a-109">Właściwości, które można ustawić, to: **etykieta** , **Opis** , **Typ** i **GeoReplicationEnabled**.</span><span class="sxs-lookup"><span data-stu-id="7554a-109">Properties that can be set are: **Label** , **Description** , **Type** and **GeoReplicationEnabled**.</span></span>

## <span data-ttu-id="7554a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7554a-110">EXAMPLES</span></span>

### <span data-ttu-id="7554a-111">Przykład 1: aktualizowanie etykiety dla konta magazynu</span><span class="sxs-lookup"><span data-stu-id="7554a-111">Example 1: Update the label for a storage account</span></span>
```
PS C:\> Set-AzureStorageAccount -StorageAccountName "ContosoStorage01" -Label "ContosoAccnt" -Description "Contoso storage account"
```

<span data-ttu-id="7554a-112">To polecenie aktualizuje właściwości **etykiety** i **opisu** konta magazynu o nazwie ContosoStorage01.</span><span class="sxs-lookup"><span data-stu-id="7554a-112">This command updates the **Label** and **Description** properties for the storage account named ContosoStorage01.</span></span>

### <span data-ttu-id="7554a-113">Przykład 2: włączanie replikacji geograficznej dla konta magazynu</span><span class="sxs-lookup"><span data-stu-id="7554a-113">Example 2: Enable geo-replication for a storage account</span></span>
```
PS C:\> Set-AzureStorageAccount -StorageAccountName "ContosoStorage01" -GeoReplicationEnabled $False
```

<span data-ttu-id="7554a-114">To polecenie ustawia właściwość **GeoReplicationEnabled** , aby $false dla konta magazynu o nazwie ContosoStorage01.</span><span class="sxs-lookup"><span data-stu-id="7554a-114">This command sets the **GeoReplicationEnabled** property to $False for the storage account named ContosoStorage01.</span></span>

### <span data-ttu-id="7554a-115">Przykład 3: wyłączanie replikacji geograficznej dla konta magazynu</span><span class="sxs-lookup"><span data-stu-id="7554a-115">Example 3: Disable geo-replication for a storage account</span></span>
```
PS C:\> Set-AzureStorageAccount -StorageAccountName "ContosoStorage01" -GeoReplicationEnabled $True
```

<span data-ttu-id="7554a-116">To polecenie ustawia właściwość **GeoReplicationEnabled** , aby $true dla konta magazynu o nazwie ContosoStorage01.</span><span class="sxs-lookup"><span data-stu-id="7554a-116">This command sets the **GeoReplicationEnabled** property to $True for the storage account named ContosoStorage01.</span></span>

## <span data-ttu-id="7554a-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7554a-117">PARAMETERS</span></span>

### <span data-ttu-id="7554a-118">— Opis</span><span class="sxs-lookup"><span data-stu-id="7554a-118">-Description</span></span>
<span data-ttu-id="7554a-119">Określa opis konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="7554a-119">Specifies a description for the storage account.</span></span>
<span data-ttu-id="7554a-120">Długość opisu może wynosić do 1024 znaków.</span><span class="sxs-lookup"><span data-stu-id="7554a-120">The description may be up to 1024 characters long.</span></span>

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

### <span data-ttu-id="7554a-121">-GeoReplicationEnabled</span><span class="sxs-lookup"><span data-stu-id="7554a-121">-GeoReplicationEnabled</span></span>
<span data-ttu-id="7554a-122">Określa, czy konto magazynu jest tworzone z włączoną replikacją geograficzną.</span><span class="sxs-lookup"><span data-stu-id="7554a-122">Specifies whether the storage account is created with the geo-replication enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: GeoReplicationEnabled
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7554a-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="7554a-123">-InformationAction</span></span>
<span data-ttu-id="7554a-124">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="7554a-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="7554a-125">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="7554a-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7554a-126">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="7554a-126">Continue</span></span>
- <span data-ttu-id="7554a-127">Ignorować</span><span class="sxs-lookup"><span data-stu-id="7554a-127">Ignore</span></span>
- <span data-ttu-id="7554a-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="7554a-128">Inquire</span></span>
- <span data-ttu-id="7554a-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="7554a-129">SilentlyContinue</span></span>
- <span data-ttu-id="7554a-130">Przestaw</span><span class="sxs-lookup"><span data-stu-id="7554a-130">Stop</span></span>
- <span data-ttu-id="7554a-131">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="7554a-131">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7554a-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="7554a-132">-InformationVariable</span></span>
<span data-ttu-id="7554a-133">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="7554a-133">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7554a-134">-Label</span><span class="sxs-lookup"><span data-stu-id="7554a-134">-Label</span></span>
<span data-ttu-id="7554a-135">Określa etykietę konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="7554a-135">Specifies a label for the storage account.</span></span>
<span data-ttu-id="7554a-136">Etykieta może mieć długość do 100 znaków.</span><span class="sxs-lookup"><span data-stu-id="7554a-136">The label may be up to 100 characters long.</span></span>

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

### <span data-ttu-id="7554a-137">-Profile</span><span class="sxs-lookup"><span data-stu-id="7554a-137">-Profile</span></span>
<span data-ttu-id="7554a-138">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7554a-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7554a-139">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="7554a-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7554a-140">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7554a-140">-StorageAccountName</span></span>
<span data-ttu-id="7554a-141">Określa nazwę konta magazynu, które zostanie zmodyfikowane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7554a-141">Specifies the name of the storage account that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7554a-142">-Type</span><span class="sxs-lookup"><span data-stu-id="7554a-142">-Type</span></span>
<span data-ttu-id="7554a-143">Określa typ konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="7554a-143">Specifies the type of the storage account.</span></span>
<span data-ttu-id="7554a-144">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="7554a-144">Valid values are:</span></span> 

- <span data-ttu-id="7554a-145">Standard_LRS</span><span class="sxs-lookup"><span data-stu-id="7554a-145">Standard_LRS</span></span>
- <span data-ttu-id="7554a-146">Standard_ZRS</span><span class="sxs-lookup"><span data-stu-id="7554a-146">Standard_ZRS</span></span>
- <span data-ttu-id="7554a-147">Standard_GRS</span><span class="sxs-lookup"><span data-stu-id="7554a-147">Standard_GRS</span></span>
- <span data-ttu-id="7554a-148">Standard_RAGRS</span><span class="sxs-lookup"><span data-stu-id="7554a-148">Standard_RAGRS</span></span>
- <span data-ttu-id="7554a-149">Premium_LRS</span><span class="sxs-lookup"><span data-stu-id="7554a-149">Premium_LRS</span></span>

<span data-ttu-id="7554a-150">Jeśli ten parametr nie jest określony, wartością domyślną jest Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="7554a-150">If this parameter is not specified, the default value is Standard_GRS.</span></span>

<span data-ttu-id="7554a-151">Wynik określania parametru *GeoReplicationEnabled* jest taki sam jak w przypadku określenia Standard_GRS w parametrze *Type* .</span><span class="sxs-lookup"><span data-stu-id="7554a-151">The effect of specifying the *GeoReplicationEnabled* parameter is the same as specifying Standard_GRS in the *Type* parameter.</span></span>

<span data-ttu-id="7554a-152">Konta Standard_ZRS lub Premium_LRS nie mogą być zmieniane na inne typy kont i odwrotnie.</span><span class="sxs-lookup"><span data-stu-id="7554a-152">Standard_ZRS or Premium_LRS accounts cannot be changed to other account types, and vice versa.</span></span>

```yaml
Type: String
Parameter Sets: AccountType
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7554a-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7554a-153">CommonParameters</span></span>
<span data-ttu-id="7554a-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7554a-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7554a-155">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7554a-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7554a-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7554a-156">INPUTS</span></span>

## <span data-ttu-id="7554a-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7554a-157">OUTPUTS</span></span>

## <span data-ttu-id="7554a-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7554a-158">NOTES</span></span>

## <span data-ttu-id="7554a-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7554a-159">RELATED LINKS</span></span>

[<span data-ttu-id="7554a-160">Get-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7554a-160">Get-AzureStorageAccount</span></span>](./Get-AzureStorageAccount.md)

[<span data-ttu-id="7554a-161">Nowe — AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7554a-161">New-AzureStorageAccount</span></span>](./New-AzureStorageAccount.md)

[<span data-ttu-id="7554a-162">Remove-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7554a-162">Remove-AzureStorageAccount</span></span>](./Remove-AzureStorageAccount.md)


