---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F1A2861F-14EF-4F67-8452-31FD498528BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCertificate.md
ms.openlocfilehash: 7eaaabf374d4ee9b43477596df06f58593c6d1e9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199611"
---
# <span data-ttu-id="99a3c-101">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="99a3c-101">Set-AzAutomationCertificate</span></span>

## <span data-ttu-id="99a3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99a3c-102">SYNOPSIS</span></span>
<span data-ttu-id="99a3c-103">Modyfikuje konfigurację certyfikatu automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="99a3c-103">Modifies the configuration of an Automation certificate.</span></span>

## <span data-ttu-id="99a3c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="99a3c-104">SYNTAX</span></span>

```
Set-AzAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path <String>] [-Exportable <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99a3c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="99a3c-105">DESCRIPTION</span></span>
<span data-ttu-id="99a3c-106">Polecenie **cmdlet Set-AzAutomationCertificate** modyfikuje konfigurację certyfikatu w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="99a3c-106">The **Set-AzAutomationCertificate** cmdlet modifies the configuration of a certificate in Azure Automation.</span></span>

## <span data-ttu-id="99a3c-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="99a3c-107">EXAMPLES</span></span>

### <span data-ttu-id="99a3c-108">Przykład 1. Modyfikowanie certyfikatu</span><span class="sxs-lookup"><span data-stu-id="99a3c-108">Example 1: Modify a certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> Set-AzAutomationCertificate -AutomationAccountName "Contos17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="99a3c-109">Pierwsze polecenie konwertuje hasło w formacie zwykłego tekstu na bezpieczny ciąg za pomocą ConvertTo-SecureString cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99a3c-109">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="99a3c-110">Polecenie przechowuje ten obiekt w $Password zmienną.</span><span class="sxs-lookup"><span data-stu-id="99a3c-110">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="99a3c-111">Drugie polecenie modyfikuje certyfikat o nazwie ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="99a3c-111">The second command modifies a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="99a3c-112">To polecenie używa hasła przechowywanego w $Password.</span><span class="sxs-lookup"><span data-stu-id="99a3c-112">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="99a3c-113">To polecenie określa nazwę konta i ścieżkę do pliku, który jest przesyłany.</span><span class="sxs-lookup"><span data-stu-id="99a3c-113">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="99a3c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99a3c-114">PARAMETERS</span></span>

### <span data-ttu-id="99a3c-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="99a3c-115">-AutomationAccountName</span></span>
<span data-ttu-id="99a3c-116">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet modyfikuje certyfikat.</span><span class="sxs-lookup"><span data-stu-id="99a3c-116">Specifies the name of the Automation account for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="99a3c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99a3c-117">-DefaultProfile</span></span>
<span data-ttu-id="99a3c-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="99a3c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="99a3c-119">— Opis</span><span class="sxs-lookup"><span data-stu-id="99a3c-119">-Description</span></span>
<span data-ttu-id="99a3c-120">Określa opis certyfikatu, który zostanie zmodyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99a3c-120">Specifies a description for the certificate that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99a3c-121">-Exportable</span><span class="sxs-lookup"><span data-stu-id="99a3c-121">-Exportable</span></span>
<span data-ttu-id="99a3c-122">Określa, czy certyfikat można wyeksportować.</span><span class="sxs-lookup"><span data-stu-id="99a3c-122">Specifies whether the certificate can be exported.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99a3c-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="99a3c-123">-Name</span></span>
<span data-ttu-id="99a3c-124">Określa nazwę certyfikatu, który zostanie zmodyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99a3c-124">Specifies the name of the certificate that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="99a3c-125">— Hasło</span><span class="sxs-lookup"><span data-stu-id="99a3c-125">-Password</span></span>
<span data-ttu-id="99a3c-126">Określa hasło pliku certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="99a3c-126">Specifies the password for the certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99a3c-127">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="99a3c-127">-Path</span></span>
<span data-ttu-id="99a3c-128">Określa ścieżkę do pliku skryptu do przekazania.</span><span class="sxs-lookup"><span data-stu-id="99a3c-128">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="99a3c-129">Plik może być plikiem cer lub plikiem pfx.</span><span class="sxs-lookup"><span data-stu-id="99a3c-129">The file can be a .cer file or a .pfx file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99a3c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99a3c-130">-ResourceGroupName</span></span>
<span data-ttu-id="99a3c-131">Określa nazwę grupy zasobów, dla której to polecenie cmdlet modyfikuje certyfikat.</span><span class="sxs-lookup"><span data-stu-id="99a3c-131">Specifies the name of the resource group for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="99a3c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99a3c-132">CommonParameters</span></span>
<span data-ttu-id="99a3c-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99a3c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99a3c-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99a3c-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99a3c-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="99a3c-135">INPUTS</span></span>

### <span data-ttu-id="99a3c-136">System.String</span><span class="sxs-lookup"><span data-stu-id="99a3c-136">System.String</span></span>

### <span data-ttu-id="99a3c-137">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="99a3c-137">System.Security.SecureString</span></span>

### <span data-ttu-id="99a3c-138">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="99a3c-138">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="99a3c-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="99a3c-139">OUTPUTS</span></span>

### <span data-ttu-id="99a3c-140">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="99a3c-140">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="99a3c-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="99a3c-141">NOTES</span></span>

## <span data-ttu-id="99a3c-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="99a3c-142">RELATED LINKS</span></span>

[<span data-ttu-id="99a3c-143">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="99a3c-143">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="99a3c-144">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="99a3c-144">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="99a3c-145">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="99a3c-145">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)


